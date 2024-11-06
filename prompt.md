CREATE DATABASE  IF NOT EXISTS `firefitdb` /*!40100 DEFAULT CHARACTER SET latin1 */;
USE `firefitdb`;
-- MySQL dump 10.13  Distrib 8.0.40, for macos14 (x86_64)
--
-- Host: mysql19.ezhostingserver.com    Database: firefitdb
-- ------------------------------------------------------
-- Server version	5.7.19

/*!40101 SET @OLD_CHARACTER_SET_CLIENT=@@CHARACTER_SET_CLIENT */;
/*!40101 SET @OLD_CHARACTER_SET_RESULTS=@@CHARACTER_SET_RESULTS */;
/*!40101 SET @OLD_COLLATION_CONNECTION=@@COLLATION_CONNECTION */;
/*!50503 SET NAMES utf8 */;
/*!40103 SET @OLD_TIME_ZONE=@@TIME_ZONE */;
/*!40103 SET TIME_ZONE='+00:00' */;
/*!40014 SET @OLD_UNIQUE_CHECKS=@@UNIQUE_CHECKS, UNIQUE_CHECKS=0 */;
/*!40014 SET @OLD_FOREIGN_KEY_CHECKS=@@FOREIGN_KEY_CHECKS, FOREIGN_KEY_CHECKS=0 */;
/*!40101 SET @OLD_SQL_MODE=@@SQL_MODE, SQL_MODE='NO_AUTO_VALUE_ON_ZERO' */;
/*!40111 SET @OLD_SQL_NOTES=@@SQL_NOTES, SQL_NOTES=0 */;

--
-- Table structure for table `_cfwheelsbase`
--

DROP TABLE IF EXISTS `_cfwheelsbase`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!50503 SET character_set_client = utf8mb4 */;
CREATE TABLE `_cfwheelsbase` (
  `ID` int(11) NOT NULL AUTO_INCREMENT,
  `tstamp` timestamp NULL DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP,
  `createdat` datetime DEFAULT NULL,
  `updatedat` datetime DEFAULT NULL,
  `deletedat` datetime DEFAULT NULL,
  PRIMARY KEY (`ID`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8;
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `_cfwheelsbase`
--

LOCK TABLES `_cfwheelsbase` WRITE;
/*!40000 ALTER TABLE `_cfwheelsbase` DISABLE KEYS */;
/*!40000 ALTER TABLE `_cfwheelsbase` ENABLE KEYS */;
UNLOCK TABLES;

--
-- Table structure for table `_competitors`
--

DROP TABLE IF EXISTS `_competitors`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!50503 SET character_set_client = utf8mb4 */;
CREATE TABLE `_competitors` (
  `id` int(11) NOT NULL DEFAULT '0',
  `aid` bigint(20) NOT NULL AUTO_INCREMENT,
  `eid` int(11) DEFAULT '0',
  `firefituserID` int(11) DEFAULT NULL,
  `tstamp` timestamp NULL DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP,
  `createdat` datetime DEFAULT NULL,
  `updatedat` datetime DEFAULT NULL,
  `deletedat` datetime DEFAULT NULL,
  `fname` text,
  `lname` text,
  `besttime` time DEFAULT '00:00:00',
  `dname` text,
  `tid` int(11) DEFAULT '0',
  `tname` text,
  `compettype` char(2) DEFAULT '',
  `sex` char(1) DEFAULT NULL,
  `age` smallint(6) DEFAULT '0',
  `rookie` char(1) DEFAULT NULL,
  `chief` char(1) DEFAULT NULL,
  PRIMARY KEY (`aid`),
  KEY `id` (`id`),
  KEY `tid` (`tid`),
  KEY `sex` (`sex`),
  KEY `age` (`age`),
  KEY `rookie` (`rookie`),
  KEY `eid` (`eid`)
) ENGINE=MyISAM AUTO_INCREMENT=2436388 DEFAULT CHARSET=utf8 COMMENT='possibly derived table from BIO table';
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `_competitors`
--

LOCK TABLES `_competitors` WRITE;
/*!40000 ALTER TABLE `_competitors` DISABLE KEYS */;
INSERT INTO `_competitors` VALUES ( ******* LONG LIST OF VALUES ******* );

/*!40000 ALTER TABLE `_competitors` ENABLE KEYS */;
UNLOCK TABLES;

--
-- Table structure for table `_contactemails`
--

DROP TABLE IF EXISTS `_contactemails`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!50503 SET character_set_client = utf8mb4 */;
CREATE TABLE `_contactemails` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `createdat` datetime DEFAULT NULL,
  `updatedat` datetime DEFAULT NULL,
  `deletedat` datetime DEFAULT NULL,
  `name` varchar(50) DEFAULT NULL,
  `email` varchar(50) DEFAULT NULL,
  `subject` varchar(200) DEFAULT NULL,
  `message` text,
  PRIMARY KEY (`id`)
) ENGINE=MyISAM AUTO_INCREMENT=1339 DEFAULT CHARSET=latin1;
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `_contactemails`
--

LOCK TABLES `_contactemails` WRITE;
/*!40000 ALTER TABLE `_contactemails` DISABLE KEYS */;
INSERT INTO `_contactemails` VALUES ( ******* LONG LIST OF VALUES ******* );
INSERT INTO `_contactemails` VALUES ( ******* LONG LIST OF VALUES ******* );

/*!40000 ALTER TABLE `_contactemails` ENABLE KEYS */;
UNLOCK TABLES;

--
-- Table structure for table `_costs`
--

DROP TABLE IF EXISTS `_costs`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!50503 SET character_set_client = utf8mb4 */;
CREATE TABLE `_costs` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `costtype` text,
  `reg` double(5,2) DEFAULT NULL,
  `reggst` double(5,2) DEFAULT NULL,
  `early` double(5,2) DEFAULT NULL,
  `earlygst` double(5,2) DEFAULT NULL,
  `regnat` char(1) DEFAULT '1',
  `eventid` int(11) NOT NULL DEFAULT '0',
  UNIQUE KEY `id` (`id`)
) ENGINE=MyISAM AUTO_INCREMENT=766 DEFAULT CHARSET=utf8;
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `_costs`
--

LOCK TABLES `_costs` WRITE;
/*!40000 ALTER TABLE `_costs` DISABLE KEYS */;
INSERT INTO `_costs` VALUES ( ******* LONG LIST OF VALUES ******* );

/*!40000 ALTER TABLE `_costs` ENABLE KEYS */;
UNLOCK TABLES;

--
-- Table structure for table `_departments`
--

DROP TABLE IF EXISTS `_departments`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!50503 SET character_set_client = utf8mb4 */;
CREATE TABLE `_departments` (
  `ID` int(11) NOT NULL AUTO_INCREMENT,
  `departmentID` int(11) DEFAULT NULL,
  `tstamp` timestamp NULL DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP,
  `createdat` datetime DEFAULT NULL,
  `updatedat` datetime DEFAULT NULL,
  `deletedat` datetime DEFAULT NULL,
  `status` varchar(10) DEFAULT NULL,
  `dnamemod` text,
  `accepted` char(1) DEFAULT '0',
  `departmenttype` varchar(30) DEFAULT NULL,
  `departmentemail` varchar(100) DEFAULT NULL,
  `address1` text,
  `address2` text,
  `city` text,
  `province` int(11) DEFAULT NULL,
  `otherprov` text,
  `country` int(11) DEFAULT NULL,
  `othercountry` varchar(50) DEFAULT NULL,
  `pcode` text,
  `phone` text,
  `phonex` text,
  `fax` text,
  `website` text,
  `departmentdescription` text,
  `numfire` int(11) DEFAULT NULL,
  `paidfire` char(1) DEFAULT NULL,
  `numpaid` int(11) DEFAULT '0',
  `volfire` char(1) DEFAULT NULL,
  `numvolunteer` int(11) DEFAULT '0',
  `chiefname` text,
  `firefitcontact1` varchar(50) DEFAULT NULL,
  `firefitcontactemail1` varchar(50) DEFAULT NULL,
  `firefitcontactphone1` varchar(20) DEFAULT NULL,
  `firefitcontact2` varchar(50) DEFAULT NULL,
  `firefitcontactemail2` varchar(50) DEFAULT NULL,
  `firefitcontactphone2` varchar(20) DEFAULT NULL,
  `firefituserID` int(11) DEFAULT NULL COMMENT 'created by firefitID',
  `numhalls` int(11) DEFAULT '1',
  `lastupdateby` int(11) DEFAULT NULL COMMENT 'firefituserID - last updated',
  PRIMARY KEY (`ID`),
  KEY `autoid` (`ID`),
  KEY `deptid` (`departmentID`)
) ENGINE=InnoDB AUTO_INCREMENT=5668 DEFAULT CHARSET=utf8;
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `_departments`
--

LOCK TABLES `_departments` WRITE;
/*!40000 ALTER TABLE `_departments` DISABLE KEYS */;
INSERT INTO `_departments` VALUES ( ******* LONG LIST OF VALUES ******* );

/*!40000 ALTER TABLE `_departments` ENABLE KEYS */;
UNLOCK TABLES;

--
-- Table structure for table `_eventcosts`
--

DROP TABLE IF EXISTS `_eventcosts`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!50503 SET character_set_client = utf8mb4 */;
CREATE TABLE `_eventcosts` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `costtype` text,
  `reg` double(5,2) DEFAULT NULL,
  `reggst` double(5,2) DEFAULT NULL,
  `early` double(5,2) DEFAULT NULL,
  `earlygst` double(5,2) DEFAULT NULL,
  `regnat` char(1) DEFAULT '1',
  `eventid` int(11) NOT NULL DEFAULT '0',
  PRIMARY KEY (`id`),
  UNIQUE KEY `id` (`id`),
  KEY `eventid` (`eventid`)
) ENGINE=MyISAM AUTO_INCREMENT=766 DEFAULT CHARSET=utf8;
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `_eventcosts`
--

LOCK TABLES `_eventcosts` WRITE;
/*!40000 ALTER TABLE `_eventcosts` DISABLE KEYS */;
INSERT INTO `_eventcosts` VALUES ( ******* LONG LIST OF VALUES ******* );

/*!40000 ALTER TABLE `_eventcosts` ENABLE KEYS */;
UNLOCK TABLES;

--
-- Table structure for table `_firefittsnbios`
--

DROP TABLE IF EXISTS `_firefittsnbios`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!50503 SET character_set_client = utf8mb4 */;
CREATE TABLE `_firefittsnbios` (
  `id` int(11) NOT NULL DEFAULT '0',
  `dept` int(11) NOT NULL DEFAULT '0',
  `fname` text NOT NULL,
  `lname` text NOT NULL,
  `sex` char(1) NOT NULL DEFAULT '',
  `age` int(11) DEFAULT NULL,
  `birthcity` text NOT NULL,
  `birthprovince` int(11) DEFAULT NULL,
  `otherbirthprov` text,
  `city` text NOT NULL,
  `province` int(11) DEFAULT NULL,
  `otherprov` text,
  `rank` int(11) NOT NULL DEFAULT '0',
  `numyears` int(11) NOT NULL DEFAULT '0',
  `numfirefit` int(11) NOT NULL DEFAULT '0',
  `whyfighter` text NOT NULL,
  `whychallenge` text NOT NULL,
  `titles` text NOT NULL,
  `greatestchallenge` text NOT NULL,
  `bestday` text NOT NULL,
  `worstday` text NOT NULL,
  `bestmoment` text NOT NULL,
  `goals` text NOT NULL,
  `hobbies` text NOT NULL,
  `advice` text NOT NULL,
  `inspiration` text NOT NULL,
  `other` text,
  `infodate` date NOT NULL DEFAULT '0000-00-00',
  KEY `infodate` (`infodate`)
) ENGINE=MyISAM DEFAULT CHARSET=utf8 COMMENT='Future Use';
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `_firefittsnbios`
--

LOCK TABLES `_firefittsnbios` WRITE;
/*!40000 ALTER TABLE `_firefittsnbios` DISABLE KEYS */;
INSERT INTO `_firefittsnbios` VALUES ( ******* LONG LIST OF VALUES ******* );

/*!40000 ALTER TABLE `_firefittsnbios` ENABLE KEYS */;
UNLOCK TABLES;

--
-- Table structure for table `_lu_deptnames`
--

DROP TABLE IF EXISTS `_lu_deptnames`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!50503 SET character_set_client = utf8mb4 */;
CREATE TABLE `_lu_deptnames` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `dname` text NOT NULL,
  `province` int(11) NOT NULL DEFAULT '0',
  `otherprov` text,
  PRIMARY KEY (`id`),
  UNIQUE KEY `id` (`id`),
  KEY `province` (`province`)
) ENGINE=MyISAM AUTO_INCREMENT=2495 DEFAULT CHARSET=utf8 COMMENT='not needed - do a lookup for active depts from departments table';
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `_lu_deptnames`
--

LOCK TABLES `_lu_deptnames` WRITE;
/*!40000 ALTER TABLE `_lu_deptnames` DISABLE KEYS */;
INSERT INTO `_lu_deptnames` VALUES ( ******* LONG LIST OF VALUES ******* );

/*!40000 ALTER TABLE `_lu_deptnames` ENABLE KEYS */;
UNLOCK TABLES;

--
-- Table structure for table `adminactivity`
--

DROP TABLE IF EXISTS `adminactivity`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!50503 SET character_set_client = utf8mb4 */;
CREATE TABLE `adminactivity` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `tStamp` timestamp NULL DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP,
  `UserID` int(11) DEFAULT NULL,
  `TeamID` int(11) DEFAULT NULL,
  `pageaction` varchar(80) DEFAULT NULL,
  `controller` varchar(30) DEFAULT NULL,
  `REMOTE_ADDR` varchar(20) DEFAULT NULL,
  `role` varchar(20) DEFAULT NULL,
  PRIMARY KEY (`id`)
) ENGINE=MyISAM AUTO_INCREMENT=371364 DEFAULT CHARSET=utf8;
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `adminactivity`
--

LOCK TABLES `adminactivity` WRITE;
/*!40000 ALTER TABLE `adminactivity` DISABLE KEYS */;
INSERT INTO `adminactivity` VALUES ( ******* LONG LIST OF VALUES ******* );

/*!40000 ALTER TABLE `adminactivity` ENABLE KEYS */;
UNLOCK TABLES;

--
-- Table structure for table `adminusers`
--

DROP TABLE IF EXISTS `adminusers`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!50503 SET character_set_client = utf8mb4 */;
CREATE TABLE `adminusers` (
  `ID` int(11) NOT NULL AUTO_INCREMENT,
  `tstamp` timestamp NULL DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP,
  `createdat` datetime DEFAULT NULL,
  `updatedat` datetime DEFAULT NULL,
  `deletedat` datetime DEFAULT NULL,
  `login` varchar(50) CHARACTER SET latin1 DEFAULT NULL,
  `password` varchar(50) CHARACTER SET latin1 DEFAULT NULL,
  `FullName` varchar(50) CHARACTER SET latin1 DEFAULT '',
  `Email` varchar(50) CHARACTER SET latin1 DEFAULT NULL,
  `Active` varchar(10) CHARACTER SET latin1 DEFAULT NULL,
  `userrole` varchar(50) CHARACTER SET latin1 DEFAULT NULL,
  PRIMARY KEY (`ID`)
) ENGINE=MyISAM AUTO_INCREMENT=981 DEFAULT CHARSET=utf8 ROW_FORMAT=DYNAMIC COMMENT='Database / Access Admin';
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `adminusers`
--

LOCK TABLES `adminusers` WRITE;
/*!40000 ALTER TABLE `adminusers` DISABLE KEYS */;
INSERT INTO `adminusers` VALUES ( ******* LONG LIST OF VALUES ******* );

/*!40000 ALTER TABLE `adminusers` ENABLE KEYS */;
UNLOCK TABLES;

--
-- Table structure for table `bios`
--

DROP TABLE IF EXISTS `bios`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!50503 SET character_set_client = utf8mb4 */;
CREATE TABLE `bios` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `firefituserID` int(11) NOT NULL,
  `departmentID` int(11) NOT NULL DEFAULT '0',
  `tstamp` timestamp NULL DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP,
  `createdat` datetime DEFAULT NULL,
  `updatedat` datetime DEFAULT NULL,
  `deletedat` datetime DEFAULT NULL,
  `infodate` date DEFAULT NULL,
  `fname` text,
  `lname` text,
  `mname` text,
  `dateofbirth` date DEFAULT NULL,
  `address1` text,
  `address2` text,
  `city` text,
  `province` int(11) DEFAULT NULL,
  `country` int(11) DEFAULT NULL,
  `countryother` varchar(50) DEFAULT NULL,
  `postalcode` varchar(7) DEFAULT NULL,
  `phone1` varchar(15) DEFAULT NULL,
  `phone2` varchar(15) DEFAULT NULL,
  `email` varchar(80) DEFAULT NULL,
  `altemail` varchar(80) DEFAULT NULL,
  `age` int(11) DEFAULT NULL,
  `emergencycontactname` varchar(40) DEFAULT NULL,
  `emergencycontactnumber` varchar(20) DEFAULT NULL,
  `heightft` int(11) DEFAULT NULL,
  `heightin` int(11) DEFAULT NULL,
  `heightcm` int(11) DEFAULT NULL,
  `weightlb` int(11) DEFAULT NULL,
  `weightkg` int(11) DEFAULT NULL,
  `paidfire` varchar(5) DEFAULT NULL,
  `paidoncall` varchar(5) DEFAULT NULL,
  `volfire` varchar(5) DEFAULT NULL,
  `rank` int(11) DEFAULT NULL,
  `numyears` int(11) DEFAULT NULL,
  `nickname` text,
  `sex` char(4) DEFAULT NULL,
  `relationstatus` varchar(20) DEFAULT NULL,
  `married` char(1) DEFAULT NULL,
  `children` char(1) DEFAULT NULL,
  `engaged` char(1) DEFAULT NULL,
  `begancompeting` int(4) DEFAULT NULL,
  `numprevchal` int(11) DEFAULT NULL,
  `prevtime` time DEFAULT NULL COMMENT 'PB Time',
  `pbminutes` int(2) DEFAULT '0',
  `pbseconds` int(2) DEFAULT '0',
  `goaltime` time DEFAULT NULL COMMENT 'Goal Time',
  `gtminutes` decimal(2,0) DEFAULT '0',
  `gtseconds` decimal(2,0) DEFAULT '0',
  `geninfo` text,
  `single` char(1) DEFAULT NULL,
  `available` char(1) DEFAULT NULL,
  `sigother` text,
  `spouse` text,
  `numkids` int(11) DEFAULT '0',
  `kidnames` text,
  `rookie` char(1) DEFAULT NULL,
  `otherprov` text,
  `spelling` text,
  `bestknownfor` text,
  `zip` varchar(5) DEFAULT 'N.A.',
  `homemail` char(1) DEFAULT '1',
  `showmid` char(1) DEFAULT '',
  `preflang` char(10) DEFAULT '',
  `mobilephone` varchar(15) DEFAULT '',
  `tshirt` char(10) DEFAULT '',
  `shirttype` varchar(10) NOT NULL DEFAULT 'T-Shirt',
  `whyfirefit` text,
  `photo` varchar(50) DEFAULT NULL,
  PRIMARY KEY (`id`),
  KEY `dept` (`departmentID`)
) ENGINE=InnoDB AUTO_INCREMENT=102559 DEFAULT CHARSET=utf8;
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `bios`
--

LOCK TABLES `bios` WRITE;
/*!40000 ALTER TABLE `bios` DISABLE KEYS */;
INSERT INTO `bios` VALUES ( ******* LONG LIST OF VALUES ******* );

/*!40000 ALTER TABLE `bios` ENABLE KEYS */;
UNLOCK TABLES;

--
-- Table structure for table `caslemailtracking`
--

DROP TABLE IF EXISTS `caslemailtracking`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!50503 SET character_set_client = utf8mb4 */;
CREATE TABLE `caslemailtracking` (
  `ID` int(11) NOT NULL AUTO_INCREMENT,
  `tstamp` timestamp NULL DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP,
  `createdat` datetime DEFAULT NULL,
  `updatedat` datetime DEFAULT NULL,
  `deletedat` datetime DEFAULT NULL,
  `firstname` varchar(30) DEFAULT NULL,
  `lastname` varchar(30) DEFAULT NULL,
  `email` varchar(40) DEFAULT NULL,
  `senttimestamp` datetime DEFAULT NULL,
  `linkuuid` varchar(80) DEFAULT NULL,
  `approvaltimestamp` datetime DEFAULT NULL,
  `expressconsent` varchar(20) DEFAULT NULL,
  `transactionalconsent` varchar(20) DEFAULT NULL,
  `donotemail` varchar(20) DEFAULT NULL,
  PRIMARY KEY (`ID`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8;
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `caslemailtracking`
--

LOCK TABLES `caslemailtracking` WRITE;
/*!40000 ALTER TABLE `caslemailtracking` DISABLE KEYS */;
/*!40000 ALTER TABLE `caslemailtracking` ENABLE KEYS */;
UNLOCK TABLES;

--
-- Table structure for table `contactemails`
--

DROP TABLE IF EXISTS `contactemails`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!50503 SET character_set_client = utf8mb4 */;
CREATE TABLE `contactemails` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `tstamp` timestamp NOT NULL DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP,
  `createdat` datetime DEFAULT NULL,
  `updatedat` datetime DEFAULT NULL,
  `deletedat` datetime DEFAULT NULL,
  `firefituserID` int(11) NOT NULL,
  `fname` text NOT NULL,
  `lname` text NOT NULL,
  `email` varchar(80) NOT NULL,
  PRIMARY KEY (`id`)
) ENGINE=MyISAM AUTO_INCREMENT=3 DEFAULT CHARSET=utf8;
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `contactemails`
--

LOCK TABLES `contactemails` WRITE;
/*!40000 ALTER TABLE `contactemails` DISABLE KEYS */;
INSERT INTO `contactemails` VALUES ( ******* LONG LIST OF VALUES ******* );

/*!40000 ALTER TABLE `contactemails` ENABLE KEYS */;
UNLOCK TABLES;

--
-- Table structure for table `credits`
--

DROP TABLE IF EXISTS `credits`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!50503 SET character_set_client = utf8mb4 */;
CREATE TABLE `credits` (
  `ID` int(11) NOT NULL AUTO_INCREMENT,
  `tstamp` timestamp NOT NULL DEFAULT CURRENT_TIMESTAMP,
  `createdat` datetime DEFAULT NULL,
  `updatedat` datetime DEFAULT NULL,
  `deletedat` datetime DEFAULT NULL,
  `userID` int(11) NOT NULL COMMENT 'The ID for the person who the registration was for (may or may not be the same as the payerID)',
  `payerID` int(11) NOT NULL COMMENT 'The ID for the person making the payment',
  `registrationID` int(11) DEFAULT NULL,
  `invoiceid` int(11) DEFAULT NULL,
  `paymentid` int(11) DEFAULT NULL,
  `eventID` int(11) NOT NULL,
  `amount` decimal(10,2) NOT NULL,
  `tx_date` timestamp NOT NULL DEFAULT CURRENT_TIMESTAMP,
  `creditnotes` text,
  PRIMARY KEY (`ID`),
  KEY `idx_payment_id` (`paymentid`),
  KEY `idx_payer_id` (`payerID`),
  KEY `idx_user_id` (`userID`),
  KEY `idx_event_id` (`eventID`),
  KEY `fk_invoice_id` (`invoiceid`),
  KEY `fk_registration_id` (`registrationID`),
  CONSTRAINT `fk_event_id` FOREIGN KEY (`eventID`) REFERENCES `events` (`id`) ON DELETE NO ACTION ON UPDATE NO ACTION,
  CONSTRAINT `fk_invoice_id` FOREIGN KEY (`invoiceid`) REFERENCES `invoices` (`ID`) ON DELETE NO ACTION ON UPDATE NO ACTION,
  CONSTRAINT `fk_payer_id` FOREIGN KEY (`payerID`) REFERENCES `firefitusers` (`ID`) ON DELETE NO ACTION ON UPDATE NO ACTION,
  CONSTRAINT `fk_payment_id` FOREIGN KEY (`paymentid`) REFERENCES `payments` (`ID`) ON DELETE NO ACTION ON UPDATE NO ACTION,
  CONSTRAINT `fk_registration_id` FOREIGN KEY (`registrationID`) REFERENCES `registrations` (`id`) ON DELETE NO ACTION ON UPDATE NO ACTION,
  CONSTRAINT `fk_user_id` FOREIGN KEY (`userID`) REFERENCES `firefitusers` (`ID`) ON DELETE NO ACTION ON UPDATE NO ACTION
) ENGINE=InnoDB AUTO_INCREMENT=159 DEFAULT CHARSET=utf8;
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `credits`
--

LOCK TABLES `credits` WRITE;
/*!40000 ALTER TABLE `credits` DISABLE KEYS */;
INSERT INTO `credits` VALUES ( ******* LONG LIST OF VALUES ******* );

/*!40000 ALTER TABLE `credits` ENABLE KEYS */;
UNLOCK TABLES;

--
-- Table structure for table `departments`
--

DROP TABLE IF EXISTS `departments`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!50503 SET character_set_client = utf8mb4 */;
CREATE TABLE `departments` (
  `ID` int(11) NOT NULL AUTO_INCREMENT,
  `departmentID` int(11) DEFAULT NULL,
  `tstamp` timestamp NULL DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP,
  `createdat` datetime DEFAULT NULL,
  `updatedat` datetime DEFAULT NULL,
  `deletedat` datetime DEFAULT NULL,
  `status` varchar(10) DEFAULT NULL,
  `dnamemod` text,
  `departmenttype` varchar(30) DEFAULT NULL,
  `departmentemail` varchar(100) DEFAULT NULL,
  `address1` text,
  `address2` text,
  `city` text,
  `province` int(11) DEFAULT NULL,
  `otherprov` text,
  `country` int(11) DEFAULT NULL,
  `othercountry` varchar(50) DEFAULT NULL,
  `pcode` text,
  `phone` text,
  `phonex` text,
  `fax` text,
  `website` text,
  `departmentdescription` text,
  `numfire` int(11) DEFAULT NULL,
  `paidfire` char(1) DEFAULT NULL,
  `numpaid` int(11) DEFAULT '0',
  `volfire` char(1) DEFAULT NULL,
  `numvolunteer` int(11) DEFAULT '0',
  `chiefname` text,
  `firefitcontact1` varchar(50) DEFAULT NULL,
  `firefitcontactemail1` varchar(50) DEFAULT NULL,
  `firefitcontactphone1` varchar(20) DEFAULT NULL,
  `firefitcontact2` varchar(50) DEFAULT NULL,
  `firefitcontactemail2` varchar(50) DEFAULT NULL,
  `firefitcontactphone2` varchar(20) DEFAULT NULL,
  `firefituserID` int(11) DEFAULT NULL COMMENT 'created by firefitID',
  `numhalls` int(11) DEFAULT '1',
  `accepted` char(1) DEFAULT '0',
  `lastupdateby` int(11) DEFAULT NULL COMMENT 'firefituserID - last updated',
  PRIMARY KEY (`ID`),
  KEY `autoid` (`ID`) USING BTREE,
  KEY `deptid` (`departmentID`) USING BTREE
) ENGINE=InnoDB AUTO_INCREMENT=6372 DEFAULT CHARSET=utf8;
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `departments`
--

LOCK TABLES `departments` WRITE;
/*!40000 ALTER TABLE `departments` DISABLE KEYS */;
INSERT INTO `departments` VALUES ( ******* LONG LIST OF VALUES ******* );

/*!40000 ALTER TABLE `departments` ENABLE KEYS */;
UNLOCK TABLES;

--
-- Table structure for table `eventcosts`
--

DROP TABLE IF EXISTS `eventcosts`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!50503 SET character_set_client = utf8mb4 */;
CREATE TABLE `eventcosts` (
  `ID` int(11) NOT NULL AUTO_INCREMENT,
  `tstamp` timestamp NULL DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP,
  `createdat` datetime DEFAULT NULL,
  `updatedat` datetime DEFAULT NULL,
  `deletedat` datetime DEFAULT NULL,
  `eventID` int(11) DEFAULT NULL,
  `eventtypeID` int(11) DEFAULT NULL,
  `price_early` decimal(10,2) NOT NULL,
  `price_regular` decimal(10,2) NOT NULL,
  `price_onsite` decimal(10,2) NOT NULL,
  `price_additional` decimal(10,2) NOT NULL,
  PRIMARY KEY (`ID`)
) ENGINE=MyISAM AUTO_INCREMENT=310 DEFAULT CHARSET=utf8;
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `eventcosts`
--

LOCK TABLES `eventcosts` WRITE;
/*!40000 ALTER TABLE `eventcosts` DISABLE KEYS */;
INSERT INTO `eventcosts` VALUES ( ******* LONG LIST OF VALUES ******* );

/*!40000 ALTER TABLE `eventcosts` ENABLE KEYS */;
UNLOCK TABLES;

--
-- Table structure for table `events`
--

DROP TABLE IF EXISTS `events`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!50503 SET character_set_client = utf8mb4 */;
CREATE TABLE `events` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `tstamp` timestamp NULL DEFAULT CURRENT_TIMESTAMP,
  `createdat` datetime DEFAULT NULL,
  `updatedat` datetime DEFAULT NULL,
  `deletedat` datetime DEFAULT NULL,
  `eventyear` int(4) DEFAULT NULL,
  `active` int(2) DEFAULT NULL,
  `status` int(11) DEFAULT NULL,
  `event` varchar(80) DEFAULT NULL,
  `startdate` date DEFAULT NULL,
  `enddate` date DEFAULT NULL,
  `address1` varchar(100) DEFAULT NULL,
  `address2` varchar(100) DEFAULT NULL,
  `city` text,
  `province` int(11) DEFAULT NULL,
  `postzip` varchar(15) DEFAULT NULL,
  `embedmaplink` text,
  `eventtype` int(11) DEFAULT '7',
  `otherprov` text,
  `regnat` char(1) DEFAULT NULL,
  `numplayers` int(11) DEFAULT NULL,
  `eventinfo1` text,
  `eventinfo2` text,
  `banquet` char(1) DEFAULT '2',
  `banquetcontact` text,
  `banquetphone` text,
  `banquetemail` text,
  `banquetetext` text,
  `banquetftext` text,
  `webpage` text,
  `corpt` char(1) DEFAULT '',
  `pricemode` varchar(20) DEFAULT '',
  `earlybirdpricecutoff` date DEFAULT NULL,
  `regularpricecutoff` date DEFAULT NULL,
  `registrationcutoff` date DEFAULT NULL,
  `maxindteam` int(5) DEFAULT '0',
  `maxnxg2` int(5) DEFAULT '0',
  `maxrelay` int(5) DEFAULT '0',
  `selectForMerge` bit(1) DEFAULT b'0',
  `seedingday` bit(1) DEFAULT NULL COMMENT 'THE DAY REQUIRED TO BE SIGNED UP FOR IF RELAY/X3',
  PRIMARY KEY (`id`),
  KEY `startdate` (`startdate`)
) ENGINE=InnoDB AUTO_INCREMENT=514 DEFAULT CHARSET=utf8;
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `events`
--

LOCK TABLES `events` WRITE;
/*!40000 ALTER TABLE `events` DISABLE KEYS */;
INSERT INTO `events` VALUES ( ******* LONG LIST OF VALUES ******* );

/*!40000 ALTER TABLE `events` ENABLE KEYS */;
UNLOCK TABLES;

--
-- Table structure for table `eventtoggles`
--

DROP TABLE IF EXISTS `eventtoggles`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!50503 SET character_set_client = utf8mb4 */;
CREATE TABLE `eventtoggles` (
  `eventtype` tinyint(4) NOT NULL,
  `mens` bit(1) NOT NULL,
  `womens` bit(1) NOT NULL,
  `mixed` bit(1) NOT NULL,
  `over40` bit(1) NOT NULL,
  `over45` bit(1) NOT NULL,
  `over50` bit(1) NOT NULL,
  `over55` bit(1) NOT NULL,
  `over60` bit(1) NOT NULL,
  `over65` bit(1) NOT NULL,
  `student` bit(1) NOT NULL,
  `industrial` bit(1) NOT NULL,
  `industrialvolunteer` bit(1) NOT NULL,
  `volunteer` bit(1) NOT NULL,
  PRIMARY KEY (`eventtype`)
) ENGINE=MyISAM DEFAULT CHARSET=utf8;
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `eventtoggles`
--

LOCK TABLES `eventtoggles` WRITE;
/*!40000 ALTER TABLE `eventtoggles` DISABLE KEYS */;
INSERT INTO `eventtoggles` VALUES ( ******* LONG LIST OF VALUES ******* );

/*!40000 ALTER TABLE `eventtoggles` ENABLE KEYS */;
UNLOCK TABLES;

--
-- Table structure for table `eventtypes`
--

DROP TABLE IF EXISTS `eventtypes`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!50503 SET character_set_client = utf8mb4 */;
CREATE TABLE `eventtypes` (
  `ID` int(11) NOT NULL AUTO_INCREMENT,
  `tstamp` timestamp NULL DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP,
  `createdat` datetime DEFAULT NULL,
  `updatedat` datetime DEFAULT NULL,
  `deletedat` datetime DEFAULT NULL,
  `eventID` int(11) DEFAULT NULL,
  `eventTypeDescription` varchar(50) DEFAULT NULL,
  `eventTypeNotes` varchar(100) DEFAULT NULL,
  PRIMARY KEY (`ID`)
) ENGINE=MyISAM AUTO_INCREMENT=6 DEFAULT CHARSET=utf8;
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `eventtypes`
--

LOCK TABLES `eventtypes` WRITE;
/*!40000 ALTER TABLE `eventtypes` DISABLE KEYS */;
INSERT INTO `eventtypes` VALUES ( ******* LONG LIST OF VALUES ******* );

/*!40000 ALTER TABLE `eventtypes` ENABLE KEYS */;
UNLOCK TABLES;

--
-- Table structure for table `firefitusers`
--

DROP TABLE IF EXISTS `firefitusers`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!50503 SET character_set_client = utf8mb4 */;
CREATE TABLE `firefitusers` (
  `ID` int(11) NOT NULL AUTO_INCREMENT,
  `tstamp` timestamp NULL DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP,
  `createdat` datetime DEFAULT NULL,
  `updatedat` datetime DEFAULT NULL,
  `deletedat` datetime DEFAULT NULL,
  `email` text NOT NULL,
  `password` text NOT NULL,
  `firstname` varchar(40) DEFAULT NULL,
  `lastname` varchar(40) DEFAULT NULL,
  `evalid` char(1) DEFAULT '0',
  `activationkey` varchar(50) DEFAULT NULL,
  `activationkeypassword` varchar(20) DEFAULT NULL,
  `activateddate` date DEFAULT NULL,
  `firelogin` text,
  `hint` int(11) DEFAULT NULL,
  `hintans` text,
  `team_id` int(6) unsigned DEFAULT NULL,
  `otherbio` char(1) DEFAULT '0',
  `createdate` date DEFAULT '0000-00-00',
  `removeflag` char(1) DEFAULT '0',
  `caslUUID` varchar(60) DEFAULT NULL,
  `caslconfirmat` datetime DEFAULT NULL,
  `caslsentat` datetime DEFAULT NULL,
  `caslpromo` char(1) DEFAULT '0',
  `caslpromodatetime` datetime DEFAULT NULL,
  `casltransactional` char(1) DEFAULT '0',
  `casltransactionaldatetime` datetime DEFAULT NULL,
  `credits` decimal(10,2) DEFAULT '0.00',
  PRIMARY KEY (`ID`),
  KEY `team_id` (`team_id`)
) ENGINE=InnoDB AUTO_INCREMENT=104369 DEFAULT CHARSET=utf8 COMMENT='FireFit Users - login/pwd table';
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `firefitusers`
--

LOCK TABLES `firefitusers` WRITE;
/*!40000 ALTER TABLE `firefitusers` DISABLE KEYS */;
INSERT INTO `firefitusers` VALUES ( ******* LONG LIST OF VALUES ******* );

/*!40000 ALTER TABLE `firefitusers` ENABLE KEYS */;
UNLOCK TABLES;

--
-- Table structure for table `invoicelines`
--

DROP TABLE IF EXISTS `invoicelines`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!50503 SET character_set_client = utf8mb4 */;
CREATE TABLE `invoicelines` (
  `ID` int(11) NOT NULL AUTO_INCREMENT,
  `tstamp` timestamp NULL DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP,
  `createdat` datetime DEFAULT NULL,
  `updatedat` datetime DEFAULT NULL,
  `deletedat` datetime DEFAULT NULL,
  `invoiceID` int(11) DEFAULT NULL,
  `registrationID` int(11) DEFAULT NULL,
  `linedescription` varchar(100) DEFAULT NULL,
  `linecost` decimal(10,2) DEFAULT NULL,
  `taxrate` decimal(10,2) DEFAULT NULL,
  `linetax` decimal(10,2) DEFAULT NULL,
  `linetotal` decimal(10,2) DEFAULT NULL,
  `taxcode` varchar(20) DEFAULT NULL,
  `taxlookupID` int(11) DEFAULT NULL,
  `firefituserID` int(11) DEFAULT NULL,
  `registeredby` int(11) DEFAULT NULL,
  `eventID` int(11) DEFAULT NULL,
  `eventname` varchar(100) DEFAULT NULL,
  `teamname` varchar(100) DEFAULT NULL,
  `sessionID` varchar(100) DEFAULT NULL,
  `autopurged` datetime DEFAULT NULL,
  PRIMARY KEY (`ID`)
) ENGINE=InnoDB AUTO_INCREMENT=39344 DEFAULT CHARSET=utf8;
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `invoicelines`
--

LOCK TABLES `invoicelines` WRITE;
/*!40000 ALTER TABLE `invoicelines` DISABLE KEYS */;
INSERT INTO `invoicelines` VALUES ( ******* LONG LIST OF VALUES ******* );

/*!40000 ALTER TABLE `invoicelines` ENABLE KEYS */;
UNLOCK TABLES;

--
-- Table structure for table `invoicelines_backup`
--

DROP TABLE IF EXISTS `invoicelines_backup`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!50503 SET character_set_client = utf8mb4 */;
CREATE TABLE `invoicelines_backup` (
  `ID` int(11) NOT NULL DEFAULT '0',
  `tstamp` timestamp NULL DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP,
  `createdat` datetime DEFAULT NULL,
  `updatedat` datetime DEFAULT NULL,
  `deletedat` datetime DEFAULT NULL,
  `invoiceID` int(11) DEFAULT NULL,
  `registrationID` int(11) DEFAULT NULL,
  `linedescription` varchar(100) CHARACTER SET utf8 DEFAULT NULL,
  `linecost` decimal(10,2) DEFAULT NULL,
  `taxrate` decimal(10,2) DEFAULT NULL,
  `linetax` decimal(10,2) DEFAULT NULL,
  `linetotal` decimal(10,2) DEFAULT NULL,
  `taxcode` varchar(20) CHARACTER SET utf8 DEFAULT NULL,
  `taxlookupID` int(11) DEFAULT NULL,
  `firefituserID` int(11) DEFAULT NULL,
  `registeredby` int(11) DEFAULT NULL,
  `eventID` int(11) DEFAULT NULL,
  `eventname` varchar(100) CHARACTER SET utf8 DEFAULT NULL,
  `teamname` varchar(100) CHARACTER SET utf8 DEFAULT NULL,
  `sessionID` varchar(100) CHARACTER SET utf8 DEFAULT NULL,
  `autopurged` datetime DEFAULT NULL
) ENGINE=InnoDB DEFAULT CHARSET=latin1;
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `invoicelines_backup`
--

LOCK TABLES `invoicelines_backup` WRITE;
/*!40000 ALTER TABLE `invoicelines_backup` DISABLE KEYS */;
INSERT INTO `invoicelines_backup` VALUES ( ******* LONG LIST OF VALUES ******* );

/*!40000 ALTER TABLE `invoicelines_backup` ENABLE KEYS */;
UNLOCK TABLES;

--
-- Table structure for table `invoices`
--

DROP TABLE IF EXISTS `invoices`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!50503 SET character_set_client = utf8mb4 */;
CREATE TABLE `invoices` (
  `ID` int(11) NOT NULL AUTO_INCREMENT,
  `tstamp` timestamp NULL DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP,
  `createdat` datetime DEFAULT NULL,
  `updatedat` datetime DEFAULT NULL,
  `deletedat` datetime DEFAULT NULL,
  `invoiceStatus` varchar(20) DEFAULT NULL,
  `firefituserID` int(11) DEFAULT NULL,
  `registeredBy` int(11) DEFAULT NULL,
  `lineTotal` decimal(10,2) DEFAULT NULL,
  `taxTotal` decimal(10,2) DEFAULT NULL,
  `invoiceTotal` decimal(10,2) DEFAULT NULL,
  `paymentID` int(11) DEFAULT NULL,
  `sessionID` varchar(100) DEFAULT NULL,
  `usernotes` text,
  `adminnotes` text,
  `autopurged` datetime DEFAULT NULL,
  PRIMARY KEY (`ID`)
) ENGINE=InnoDB AUTO_INCREMENT=15213 DEFAULT CHARSET=utf8;
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `invoices`
--

LOCK TABLES `invoices` WRITE;
/*!40000 ALTER TABLE `invoices` DISABLE KEYS */;
INSERT INTO `invoices` VALUES ( ******* LONG LIST OF VALUES ******* );

/*!40000 ALTER TABLE `invoices` ENABLE KEYS */;
UNLOCK TABLES;

--
-- Table structure for table `invoices_backup`
--

DROP TABLE IF EXISTS `invoices_backup`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!50503 SET character_set_client = utf8mb4 */;
CREATE TABLE `invoices_backup` (
  `ID` int(11) NOT NULL DEFAULT '0',
  `tstamp` timestamp NULL DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP,
  `createdat` datetime DEFAULT NULL,
  `updatedat` datetime DEFAULT NULL,
  `deletedat` datetime DEFAULT NULL,
  `invoiceStatus` varchar(20) CHARACTER SET utf8 DEFAULT NULL,
  `firefituserID` int(11) DEFAULT NULL,
  `registeredBy` int(11) DEFAULT NULL,
  `lineTotal` decimal(10,2) DEFAULT NULL,
  `taxTotal` decimal(10,2) DEFAULT NULL,
  `invoiceTotal` decimal(10,2) DEFAULT NULL,
  `paymentID` int(11) DEFAULT NULL,
  `sessionID` varchar(100) CHARACTER SET utf8 DEFAULT NULL,
  `usernotes` text CHARACTER SET utf8,
  `adminnotes` text CHARACTER SET utf8,
  `autopurged` datetime DEFAULT NULL
) ENGINE=InnoDB DEFAULT CHARSET=latin1;
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `invoices_backup`
--

LOCK TABLES `invoices_backup` WRITE;
/*!40000 ALTER TABLE `invoices_backup` DISABLE KEYS */;
INSERT INTO `invoices_backup` VALUES ( ******* LONG LIST OF VALUES ******* );

/*!40000 ALTER TABLE `invoices_backup` ENABLE KEYS */;
UNLOCK TABLES;

--
-- Table structure for table `lu_cholesterollevels`
--

DROP TABLE IF EXISTS `lu_cholesterollevels`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!50503 SET character_set_client = utf8mb4 */;
CREATE TABLE `lu_cholesterollevels` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `typecholesterol` text,
  `active` int(2) DEFAULT NULL,
  `sortorder` int(2) DEFAULT NULL,
  PRIMARY KEY (`id`)
) ENGINE=MyISAM AUTO_INCREMENT=8 DEFAULT CHARSET=utf8 COMMENT='Lookup - Risko';
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `lu_cholesterollevels`
--

LOCK TABLES `lu_cholesterollevels` WRITE;
/*!40000 ALTER TABLE `lu_cholesterollevels` DISABLE KEYS */;
INSERT INTO `lu_cholesterollevels` VALUES ( ******* LONG LIST OF VALUES ******* );

/*!40000 ALTER TABLE `lu_cholesterollevels` ENABLE KEYS */;
UNLOCK TABLES;

--
-- Table structure for table `lu_countrys`
--

DROP TABLE IF EXISTS `lu_countrys`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!50503 SET character_set_client = utf8mb4 */;
CREATE TABLE `lu_countrys` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `country` text,
  `active` int(11) DEFAULT NULL,
  `sortorder` int(11) DEFAULT NULL,
  PRIMARY KEY (`id`)
) ENGINE=MyISAM AUTO_INCREMENT=10 DEFAULT CHARSET=utf8 COMMENT='Lookup';
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `lu_countrys`
--

LOCK TABLES `lu_countrys` WRITE;
/*!40000 ALTER TABLE `lu_countrys` DISABLE KEYS */;
INSERT INTO `lu_countrys` VALUES ( ******* LONG LIST OF VALUES ******* );

/*!40000 ALTER TABLE `lu_countrys` ENABLE KEYS */;
UNLOCK TABLES;

--
-- Table structure for table `lu_cvrelatives`
--

DROP TABLE IF EXISTS `lu_cvrelatives`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!50503 SET character_set_client = utf8mb4 */;
CREATE TABLE `lu_cvrelatives` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `heredity` text,
  `active` int(2) DEFAULT NULL,
  `sortorder` int(2) DEFAULT NULL,
  PRIMARY KEY (`id`)
) ENGINE=MyISAM AUTO_INCREMENT=8 DEFAULT CHARSET=utf8 COMMENT='Lookup - Risko';
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `lu_cvrelatives`
--

LOCK TABLES `lu_cvrelatives` WRITE;
/*!40000 ALTER TABLE `lu_cvrelatives` DISABLE KEYS */;
INSERT INTO `lu_cvrelatives` VALUES ( ******* LONG LIST OF VALUES ******* );

/*!40000 ALTER TABLE `lu_cvrelatives` ENABLE KEYS */;
UNLOCK TABLES;

--
-- Table structure for table `lu_eventstatuslevels`
--

DROP TABLE IF EXISTS `lu_eventstatuslevels`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!50503 SET character_set_client = utf8mb4 */;
CREATE TABLE `lu_eventstatuslevels` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `status` text,
  `active` int(11) DEFAULT NULL,
  PRIMARY KEY (`id`)
) ENGINE=MyISAM AUTO_INCREMENT=12 DEFAULT CHARSET=utf8;
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `lu_eventstatuslevels`
--

LOCK TABLES `lu_eventstatuslevels` WRITE;
/*!40000 ALTER TABLE `lu_eventstatuslevels` DISABLE KEYS */;
INSERT INTO `lu_eventstatuslevels` VALUES ( ******* LONG LIST OF VALUES ******* );

/*!40000 ALTER TABLE `lu_eventstatuslevels` ENABLE KEYS */;
UNLOCK TABLES;

--
-- Table structure for table `lu_eventtypes`
--

DROP TABLE IF EXISTS `lu_eventtypes`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!50503 SET character_set_client = utf8mb4 */;
CREATE TABLE `lu_eventtypes` (
  `ID` int(3) NOT NULL AUTO_INCREMENT,
  `eventtype` varchar(50) NOT NULL,
  `active` int(11) DEFAULT NULL,
  `maxusers` int(11) DEFAULT NULL,
  PRIMARY KEY (`ID`)
) ENGINE=MyISAM AUTO_INCREMENT=8 DEFAULT CHARSET=utf8;
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `lu_eventtypes`
--

LOCK TABLES `lu_eventtypes` WRITE;
/*!40000 ALTER TABLE `lu_eventtypes` DISABLE KEYS */;
INSERT INTO `lu_eventtypes` VALUES ( ******* LONG LIST OF VALUES ******* );

/*!40000 ALTER TABLE `lu_eventtypes` ENABLE KEYS */;
UNLOCK TABLES;

--
-- Table structure for table `lu_exercisehabits`
--

DROP TABLE IF EXISTS `lu_exercisehabits`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!50503 SET character_set_client = utf8mb4 */;
CREATE TABLE `lu_exercisehabits` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `typeofhabits` text,
  `active` int(11) DEFAULT NULL,
  `sortorder` int(11) DEFAULT NULL,
  PRIMARY KEY (`id`)
) ENGINE=MyISAM AUTO_INCREMENT=8 DEFAULT CHARSET=utf8 COMMENT='Lookup - Risko';
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `lu_exercisehabits`
--

LOCK TABLES `lu_exercisehabits` WRITE;
/*!40000 ALTER TABLE `lu_exercisehabits` DISABLE KEYS */;
INSERT INTO `lu_exercisehabits` VALUES ( ******* LONG LIST OF VALUES ******* );

/*!40000 ALTER TABLE `lu_exercisehabits` ENABLE KEYS */;
UNLOCK TABLES;

--
-- Table structure for table `lu_hints`
--

DROP TABLE IF EXISTS `lu_hints`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!50503 SET character_set_client = utf8mb4 */;
CREATE TABLE `lu_hints` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `hint` text,
  PRIMARY KEY (`id`)
) ENGINE=MyISAM AUTO_INCREMENT=9 DEFAULT CHARSET=utf8;
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `lu_hints`
--

LOCK TABLES `lu_hints` WRITE;
/*!40000 ALTER TABLE `lu_hints` DISABLE KEYS */;
INSERT INTO `lu_hints` VALUES ( ******* LONG LIST OF VALUES ******* );

/*!40000 ALTER TABLE `lu_hints` ENABLE KEYS */;
UNLOCK TABLES;

--
-- Table structure for table `lu_paymenttypes`
--

DROP TABLE IF EXISTS `lu_paymenttypes`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!50503 SET character_set_client = utf8mb4 */;
CREATE TABLE `lu_paymenttypes` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `paytype` text,
  PRIMARY KEY (`id`)
) ENGINE=MyISAM AUTO_INCREMENT=11 DEFAULT CHARSET=utf8;
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `lu_paymenttypes`
--

LOCK TABLES `lu_paymenttypes` WRITE;
/*!40000 ALTER TABLE `lu_paymenttypes` DISABLE KEYS */;
INSERT INTO `lu_paymenttypes` VALUES (1,'Visa Credit Card'),(3,'Mastercard'),(5,'Purchase Order/Cheque'),(9,'Host Comp'),(10,'Nationals');
/*!40000 ALTER TABLE `lu_paymenttypes` ENABLE KEYS */;
UNLOCK TABLES;

--
-- Table structure for table `lu_provinces`
--

DROP TABLE IF EXISTS `lu_provinces`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!50503 SET character_set_client = utf8mb4 */;
CREATE TABLE `lu_provinces` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `prov` text,
  `short` char(2) DEFAULT NULL,
  `taxrate` decimal(10,0) DEFAULT NULL,
  `taxcode` varchar(20) DEFAULT NULL,
  `active` varchar(255) DEFAULT NULL,
  `sortorder` int(11) DEFAULT NULL,
  PRIMARY KEY (`id`)
) ENGINE=MyISAM AUTO_INCREMENT=16 DEFAULT CHARSET=utf8;
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `lu_provinces`
--

LOCK TABLES `lu_provinces` WRITE;
/*!40000 ALTER TABLE `lu_provinces` DISABLE KEYS */;
INSERT INTO `lu_provinces` VALUES ( ******* LONG LIST OF VALUES ******* );

/*!40000 ALTER TABLE `lu_provinces` ENABLE KEYS */;
UNLOCK TABLES;

--
-- Table structure for table `lu_ranks`
--

DROP TABLE IF EXISTS `lu_ranks`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!50503 SET character_set_client = utf8mb4 */;
CREATE TABLE `lu_ranks` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `rank` text,
  `ranktype` varchar(10) DEFAULT NULL,
  `active` int(11) DEFAULT NULL,
  `sortorder` int(11) DEFAULT NULL,
  `grouping` varchar(10) DEFAULT NULL,
  PRIMARY KEY (`id`)
) ENGINE=MyISAM AUTO_INCREMENT=120 DEFAULT CHARSET=utf8;
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `lu_ranks`
--

LOCK TABLES `lu_ranks` WRITE;
/*!40000 ALTER TABLE `lu_ranks` DISABLE KEYS */;
INSERT INTO `lu_ranks` VALUES ( ******* LONG LIST OF VALUES ******* );

/*!40000 ALTER TABLE `lu_ranks` ENABLE KEYS */;
UNLOCK TABLES;

--
-- Table structure for table `lu_regtypes`
--

DROP TABLE IF EXISTS `lu_regtypes`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!50503 SET character_set_client = utf8mb4 */;
CREATE TABLE `lu_regtypes` (
  `typeid` char(1) NOT NULL DEFAULT '',
  `typedesc` text NOT NULL,
  PRIMARY KEY (`typeid`)
) ENGINE=MyISAM DEFAULT CHARSET=utf8;
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `lu_regtypes`
--

LOCK TABLES `lu_regtypes` WRITE;
/*!40000 ALTER TABLE `lu_regtypes` DISABLE KEYS */;
INSERT INTO `lu_regtypes` VALUES ('1','Competitor - Team'),('2','Competitor - Individual');
/*!40000 ALTER TABLE `lu_regtypes` ENABLE KEYS */;
UNLOCK TABLES;

--
-- Table structure for table `lu_runtypes`
--

DROP TABLE IF EXISTS `lu_runtypes`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!50503 SET character_set_client = utf8mb4 */;
CREATE TABLE `lu_runtypes` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `rundesc` text NOT NULL,
  `age` int(11) NOT NULL DEFAULT '0',
  `age2` smallint(6) NOT NULL DEFAULT '0',
  `sex` tinyint(4) NOT NULL DEFAULT '0',
  `rookies` char(1) NOT NULL DEFAULT '',
  `chiefs` char(1) NOT NULL DEFAULT '',
  `compet` char(1) NOT NULL DEFAULT '',
  PRIMARY KEY (`id`),
  KEY `age` (`age`,`sex`),
  KEY `rookies` (`rookies`,`chiefs`),
  KEY `age2` (`age2`),
  KEY `compet` (`compet`)
) ENGINE=MyISAM AUTO_INCREMENT=16 DEFAULT CHARSET=utf8;
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `lu_runtypes`
--

LOCK TABLES `lu_runtypes` WRITE;
/*!40000 ALTER TABLE `lu_runtypes` DISABLE KEYS */;
INSERT INTO `lu_runtypes` VALUES ( ******* LONG LIST OF VALUES ******* );

/*!40000 ALTER TABLE `lu_runtypes` ENABLE KEYS */;
UNLOCK TABLES;

--
-- Table structure for table `lu_settings__regions`
--

DROP TABLE IF EXISTS `lu_settings__regions`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!50503 SET character_set_client = utf8mb4 */;
CREATE TABLE `lu_settings__regions` (
  `region_id` int(3) NOT NULL AUTO_INCREMENT,
  `region_name` varchar(155) NOT NULL,
  PRIMARY KEY (`region_id`)
) ENGINE=MyISAM AUTO_INCREMENT=13 DEFAULT CHARSET=utf8;
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `lu_settings__regions`
--

LOCK TABLES `lu_settings__regions` WRITE;
/*!40000 ALTER TABLE `lu_settings__regions` DISABLE KEYS */;
INSERT INTO `lu_settings__regions` VALUES (1,'Pacific'),(2,'Southern Ontario'),(3,'Prairie'),(4,'Eastern Ontario'),(5,'Atlantic'),(6,'Eastern Quebec'),(12,'Western Quebec'),(11,'GTA');
/*!40000 ALTER TABLE `lu_settings__regions` ENABLE KEYS */;
UNLOCK TABLES;

--
-- Table structure for table `lu_settings__relay_types`
--

DROP TABLE IF EXISTS `lu_settings__relay_types`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!50503 SET character_set_client = utf8mb4 */;
CREATE TABLE `lu_settings__relay_types` (
  `relay_type_id` int(3) NOT NULL AUTO_INCREMENT,
  `relay_type` varchar(155) NOT NULL,
  PRIMARY KEY (`relay_type_id`)
) ENGINE=MyISAM AUTO_INCREMENT=5 DEFAULT CHARSET=utf8;
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `lu_settings__relay_types`
--

LOCK TABLES `lu_settings__relay_types` WRITE;
/*!40000 ALTER TABLE `lu_settings__relay_types` DISABLE KEYS */;
INSERT INTO `lu_settings__relay_types` VALUES (1,'Team'),(2,'Team Relay'),(3,'NXG2 Relay'),(4,'Individual');
/*!40000 ALTER TABLE `lu_settings__relay_types` ENABLE KEYS */;
UNLOCK TABLES;

--
-- Table structure for table `lu_teamgroups`
--

DROP TABLE IF EXISTS `lu_teamgroups`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!50503 SET character_set_client = utf8mb4 */;
CREATE TABLE `lu_teamgroups` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `groupname` varchar(50) DEFAULT NULL,
  `groupsort` int(2) DEFAULT NULL,
  `maxage` int(11) DEFAULT NULL,
  `minage` int(11) DEFAULT NULL,
  `maxageteam` int(11) DEFAULT NULL,
  `maxagerelay` int(11) DEFAULT NULL,
  `maxagex3` int(11) DEFAULT NULL,
  `sex` varchar(10) DEFAULT NULL,
  `rank` varchar(10) DEFAULT NULL,
  `paidfire` varchar(10) DEFAULT NULL,
  `paidoncall` varchar(10) DEFAULT NULL,
  `volfire` varchar(10) DEFAULT NULL,
  `x3presortorder` int(3) DEFAULT NULL,
  `priority` tinyint(2) DEFAULT NULL,
  `team` bit(1) NOT NULL,
  `relay` bit(1) NOT NULL,
  `x3` bit(1) NOT NULL,
  PRIMARY KEY (`id`)
) ENGINE=InnoDB AUTO_INCREMENT=33 DEFAULT CHARSET=utf8;
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `lu_teamgroups`
--

LOCK TABLES `lu_teamgroups` WRITE;
/*!40000 ALTER TABLE `lu_teamgroups` DISABLE KEYS */;
INSERT INTO `lu_teamgroups` VALUES ( ******* LONG LIST OF VALUES ******* );

/*!40000 ALTER TABLE `lu_teamgroups` ENABLE KEYS */;
UNLOCK TABLES;

--
-- Table structure for table `lu_tobaccousers`
--

DROP TABLE IF EXISTS `lu_tobaccousers`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!50503 SET character_set_client = utf8mb4 */;
CREATE TABLE `lu_tobaccousers` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `typeofuse` text,
  `active` int(11) DEFAULT NULL,
  `sortorder` int(11) DEFAULT NULL,
  PRIMARY KEY (`id`)
) ENGINE=MyISAM AUTO_INCREMENT=9 DEFAULT CHARSET=utf8 COMMENT='Lookup - Risko';
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `lu_tobaccousers`
--

LOCK TABLES `lu_tobaccousers` WRITE;
/*!40000 ALTER TABLE `lu_tobaccousers` DISABLE KEYS */;
INSERT INTO `lu_tobaccousers` VALUES ( ******* LONG LIST OF VALUES ******* );

/*!40000 ALTER TABLE `lu_tobaccousers` ENABLE KEYS */;
UNLOCK TABLES;

--
-- Table structure for table `nationaldays`
--

DROP TABLE IF EXISTS `nationaldays`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!50503 SET character_set_client = utf8mb4 */;
CREATE TABLE `nationaldays` (
  `id` int(11) NOT NULL DEFAULT '0',
  `createdat` datetime DEFAULT NULL,
  `updatedat` datetime DEFAULT NULL,
  `deletedat` datetime DEFAULT NULL,
  `teamwc` bit(1) DEFAULT b'0',
  `teambye` bit(1) DEFAULT b'0',
  `teamrelaywc` bit(1) DEFAULT b'0',
  `teamrelaybye` bit(1) DEFAULT b'0',
  `tech2relaywc` bit(1) DEFAULT NULL,
  `tech2relaybye` bit(1) DEFAULT NULL,
  `individualwc` bit(1) DEFAULT b'0',
  `individualbye` bit(1) DEFAULT b'0',
  PRIMARY KEY (`id`)
) ENGINE=MyISAM DEFAULT CHARSET=utf8;
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `nationaldays`
--

LOCK TABLES `nationaldays` WRITE;
/*!40000 ALTER TABLE `nationaldays` DISABLE KEYS */;
INSERT INTO `nationaldays` VALUES ( ******* LONG LIST OF VALUES ******* );

/*!40000 ALTER TABLE `nationaldays` ENABLE KEYS */;
UNLOCK TABLES;

--
-- Table structure for table `paymentcodes`
--

DROP TABLE IF EXISTS `paymentcodes`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!50503 SET character_set_client = utf8mb4 */;
CREATE TABLE `paymentcodes` (
  `ID` int(11) NOT NULL AUTO_INCREMENT,
  `tstamp` timestamp NULL DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP,
  `createdat` datetime DEFAULT NULL,
  `updatedat` datetime DEFAULT NULL,
  `deletedat` datetime DEFAULT NULL,
  `paycode` varchar(20) DEFAULT NULL,
  `codetype` varchar(20) DEFAULT NULL,
  `percentdiscount` int(11) DEFAULT NULL,
  `amountdiscount` int(11) DEFAULT NULL,
  `startdate` date DEFAULT NULL,
  `enddate` date DEFAULT NULL,
  `usecountlimit` int(11) DEFAULT NULL COMMENT 'limt count for number of uses',
  `poreferencenumber` int(11) DEFAULT NULL,
  `podepartmentID` int(11) DEFAULT NULL,
  `povalue` int(11) DEFAULT NULL,
  `poeventID` int(11) DEFAULT NULL,
  `ponotes` text,
  `paycodenotes` text,
  `pocontact` varchar(30) DEFAULT NULL,
  `adminnotes` text,
  PRIMARY KEY (`ID`)
) ENGINE=InnoDB AUTO_INCREMENT=180 DEFAULT CHARSET=utf8 COMMENT='payment/POs/Coupon Codes';
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `paymentcodes`
--

LOCK TABLES `paymentcodes` WRITE;
/*!40000 ALTER TABLE `paymentcodes` DISABLE KEYS */;
INSERT INTO `paymentcodes` VALUES ( ******* LONG LIST OF VALUES ******* );

/*!40000 ALTER TABLE `paymentcodes` ENABLE KEYS */;
UNLOCK TABLES;

--
-- Table structure for table `payments`
--

DROP TABLE IF EXISTS `payments`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!50503 SET character_set_client = utf8mb4 */;
CREATE TABLE `payments` (
  `ID` int(11) NOT NULL AUTO_INCREMENT,
  `tstamp` timestamp NULL DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP,
  `createdat` datetime DEFAULT NULL,
  `updatedat` datetime DEFAULT NULL,
  `deletedat` datetime DEFAULT NULL,
  `invoiceID` int(11) DEFAULT NULL,
  `invoicelinetotal` decimal(10,2) DEFAULT NULL,
  `invoicetaxtotal` decimal(10,2) DEFAULT NULL,
  `invoicetotal` decimal(10,2) DEFAULT NULL,
  `paymenttype` varchar(20) DEFAULT NULL,
  `paymentstatus` varchar(20) DEFAULT NULL,
  `firefituserID` int(11) DEFAULT NULL,
  `purchaseorder` varchar(20) DEFAULT NULL,
  `ccfullname` varchar(50) DEFAULT NULL,
  `ccnumber` varchar(80) DEFAULT NULL,
  `ccexpirymonth` varchar(2) DEFAULT NULL,
  `ccexpiryyear` varchar(4) DEFAULT NULL,
  `ccCVSNumber` varchar(3) DEFAULT NULL,
  `ccauthnumber` varchar(30) DEFAULT NULL,
  `paynotes` text,
  `usernotes` text,
  `paywithcredits` int(1) DEFAULT '0',
  `creditsused` decimal(10,2) DEFAULT '0.00',
  PRIMARY KEY (`ID`)
) ENGINE=InnoDB AUTO_INCREMENT=6609 DEFAULT CHARSET=utf8;
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `payments`
--

LOCK TABLES `payments` WRITE;
/*!40000 ALTER TABLE `payments` DISABLE KEYS */;
INSERT INTO `payments` VALUES ( ******* LONG LIST OF VALUES ******* );

/*!40000 ALTER TABLE `payments` ENABLE KEYS */;
UNLOCK TABLES;

--
-- Table structure for table `payments_backup`
--

DROP TABLE IF EXISTS `payments_backup`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!50503 SET character_set_client = utf8mb4 */;
CREATE TABLE `payments_backup` (
  `ID` int(11) NOT NULL DEFAULT '0',
  `tstamp` timestamp NULL DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP,
  `createdat` datetime DEFAULT NULL,
  `updatedat` datetime DEFAULT NULL,
  `deletedat` datetime DEFAULT NULL,
  `invoiceID` int(11) DEFAULT NULL,
  `invoicelinetotal` decimal(10,2) DEFAULT NULL,
  `invoicetaxtotal` decimal(10,2) DEFAULT NULL,
  `invoicetotal` decimal(10,2) DEFAULT NULL,
  `paymenttype` varchar(20) CHARACTER SET utf8 DEFAULT NULL,
  `paymentstatus` varchar(20) CHARACTER SET utf8 DEFAULT NULL,
  `firefituserID` int(11) DEFAULT NULL,
  `purchaseorder` varchar(20) CHARACTER SET utf8 DEFAULT NULL,
  `ccfullname` varchar(50) CHARACTER SET utf8 DEFAULT NULL,
  `ccnumber` varchar(80) CHARACTER SET utf8 DEFAULT NULL,
  `ccexpirymonth` varchar(2) CHARACTER SET utf8 DEFAULT NULL,
  `ccexpiryyear` varchar(4) CHARACTER SET utf8 DEFAULT NULL,
  `ccCVSNumber` varchar(3) CHARACTER SET utf8 DEFAULT NULL,
  `ccauthnumber` varchar(30) CHARACTER SET utf8 DEFAULT NULL,
  `paynotes` text CHARACTER SET utf8,
  `usernotes` text CHARACTER SET utf8,
  `paywithcredits` int(1) DEFAULT '0',
  `creditsused` decimal(10,2) DEFAULT '0.00'
) ENGINE=InnoDB DEFAULT CHARSET=latin1;
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `payments_backup`
--

LOCK TABLES `payments_backup` WRITE;
/*!40000 ALTER TABLE `payments_backup` DISABLE KEYS */;
INSERT INTO `payments_backup` VALUES ( ******* LONG LIST OF VALUES ******* );

/*!40000 ALTER TABLE `payments_backup` ENABLE KEYS */;
UNLOCK TABLES;

--
-- Table structure for table `registrations`
--

DROP TABLE IF EXISTS `registrations`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!50503 SET character_set_client = utf8mb4 */;
CREATE TABLE `registrations` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `tstamp` timestamp NULL DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP,
  `createdat` datetime DEFAULT NULL,
  `updatedat` datetime DEFAULT NULL,
  `deletedat` datetime DEFAULT NULL,
  `registeredBy` int(11) DEFAULT NULL,
  `firefituserID` int(11) DEFAULT NULL,
  `eventID` int(11) DEFAULT NULL,
  `eventtypeID` int(11) DEFAULT NULL,
  `teamID` varchar(40) DEFAULT NULL,
  `departmentID` int(11) DEFAULT NULL,
  `regstatus` varchar(30) DEFAULT NULL,
  `paidstatus` varchar(30) DEFAULT NULL,
  `teamName` varchar(100) DEFAULT NULL,
  `teamregflag` char(1) DEFAULT '0',
  `sponsors` varchar(200) DEFAULT NULL,
  `runorder` int(11) DEFAULT '0',
  `nxrunorder` int(11) DEFAULT '0' COMMENT 'subsort for NxG2 layer order in a team',
  `teamcategory` varchar(5) DEFAULT '0',
  `indcategory` varchar(30) DEFAULT NULL,
  `invoiceID` int(11) DEFAULT NULL,
  `invoicelineID` int(11) DEFAULT NULL,
  `paymentID` int(11) DEFAULT NULL,
  `sessionID` varchar(100) DEFAULT NULL,
  `autopurged` datetime DEFAULT NULL,
  `funteam` varchar(2) DEFAULT '0',
  `quickreg` varchar(2) DEFAULT '0',
  `natreg` varchar(2) DEFAULT '0',
  `prevteamID` varchar(40) DEFAULT NULL,
  `natregtype` varchar(12) DEFAULT NULL,
  `remoteip` varchar(20) DEFAULT NULL,
  `finaltransfer` varchar(5) DEFAULT NULL,
  `copylinkflag` varchar(60) DEFAULT NULL,
  `wcquickteam` varchar(2) DEFAULT '0',
  `note` text,
  PRIMARY KEY (`id`),
  KEY `firefituserID` (`firefituserID`),
  KEY `eventID` (`eventID`),
  KEY `teamID` (`teamID`) USING BTREE
) ENGINE=InnoDB AUTO_INCREMENT=48215 DEFAULT CHARSET=utf8 COMMENT='This links to the event table - listing of events';
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `registrations`
--

LOCK TABLES `registrations` WRITE;
/*!40000 ALTER TABLE `registrations` DISABLE KEYS */;
INSERT INTO `registrations` VALUES ( ******* LONG LIST OF VALUES ******* );

/*!40000 ALTER TABLE `registrations` ENABLE KEYS */;
UNLOCK TABLES;

--
-- Table structure for table `results`
--

DROP TABLE IF EXISTS `results`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!50503 SET character_set_client = utf8mb4 */;
CREATE TABLE `results` (
  `ID` int(11) NOT NULL AUTO_INCREMENT,
  `tstamp` timestamp NULL DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP,
  `createdat` datetime DEFAULT NULL,
  `updatedat` datetime DEFAULT NULL,
  `deletedat` datetime DEFAULT NULL,
  `EventID` int(11) DEFAULT NULL,
  `EventTypeID` int(11) DEFAULT NULL,
  `firefituserID` int(11) DEFAULT NULL,
  `deptID` int(11) DEFAULT NULL,
  `registrationID` int(11) DEFAULT NULL,
  `TeamID` varchar(80) DEFAULT NULL,
  `timeminutes` int(2) DEFAULT '0',
  `timeseconds` int(2) DEFAULT '0',
  `time100ths` int(3) DEFAULT '0',
  `penalty` varchar(40) DEFAULT NULL COMMENT 'Penalty Flag - 1/0',
  `penaltytime` int(5) DEFAULT '0',
  `status` varchar(5) DEFAULT NULL,
  `byestatus` varchar(5) DEFAULT NULL,
  `wcstatus` varchar(5) DEFAULT NULL,
  `relayfinishposition` varchar(5) DEFAULT NULL,
  `finishstatus` varchar(20) DEFAULT NULL,
  `natTeamCreate` int(11) DEFAULT '0',
  PRIMARY KEY (`ID`),
  KEY `teamID` (`TeamID`) USING BTREE
) ENGINE=InnoDB AUTO_INCREMENT=24292 DEFAULT CHARSET=utf8;
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `results`
--

LOCK TABLES `results` WRITE;
/*!40000 ALTER TABLE `results` DISABLE KEYS */;
INSERT INTO `results` VALUES ( ******* LONG LIST OF VALUES ******* );

/*!40000 ALTER TABLE `results` ENABLE KEYS */;
UNLOCK TABLES;

--
-- Table structure for table `resultsnxg2`
--

DROP TABLE IF EXISTS `resultsnxg2`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!50503 SET character_set_client = utf8mb4 */;
CREATE TABLE `resultsnxg2` (
  `ID` int(11) NOT NULL AUTO_INCREMENT,
  `tstamp` timestamp NULL DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP,
  `createdat` datetime DEFAULT NULL,
  `updatedat` datetime DEFAULT NULL,
  `deletedat` datetime DEFAULT NULL,
  `EventID` int(11) DEFAULT NULL,
  `EventTypeID` int(11) DEFAULT NULL,
  `TeamID` varchar(80) DEFAULT NULL,
  `departmentID` int(11) DEFAULT NULL,
  `timeminutes` int(2) DEFAULT '0',
  `timeseconds` int(2) DEFAULT '0',
  `time100ths` int(3) DEFAULT '0',
  `penalty` varchar(40) DEFAULT NULL COMMENT 'Penalty Flag - 1/0',
  `penaltytime` int(5) DEFAULT '0',
  `status` varchar(5) DEFAULT NULL,
  `byestatus` varchar(5) DEFAULT NULL,
  `wcstatus` varchar(5) DEFAULT NULL,
  `relayfinishposition` varchar(5) DEFAULT NULL,
  `finishstatus` varchar(20) DEFAULT NULL,
  PRIMARY KEY (`ID`),
  KEY `teamID` (`TeamID`) USING BTREE
) ENGINE=InnoDB AUTO_INCREMENT=2972 DEFAULT CHARSET=utf8;
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `resultsnxg2`
--

LOCK TABLES `resultsnxg2` WRITE;
/*!40000 ALTER TABLE `resultsnxg2` DISABLE KEYS */;
INSERT INTO `resultsnxg2` VALUES ( ******* LONG LIST OF VALUES ******* );

/*!40000 ALTER TABLE `resultsnxg2` ENABLE KEYS */;
UNLOCK TABLES;

--
-- Table structure for table `riskos`
--

DROP TABLE IF EXISTS `riskos`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!50503 SET character_set_client = utf8mb4 */;
CREATE TABLE `riskos` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `firefituserID` int(11) DEFAULT NULL,
  `tstamp` timestamp NULL DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP,
  `createdat` datetime DEFAULT NULL,
  `updatedat` datetime DEFAULT NULL,
  `deletedat` datetime DEFAULT NULL,
  `tobaccouse` int(11) DEFAULT NULL,
  `exercisehabits` int(11) DEFAULT NULL,
  `heredity` int(11) DEFAULT NULL,
  `cholesterol` int(11) DEFAULT NULL,
  `hearttrouble` char(1) DEFAULT NULL,
  `pains` char(1) DEFAULT NULL,
  `faint` char(1) DEFAULT NULL,
  `highbp` char(1) DEFAULT NULL,
  `bonejoint` char(1) DEFAULT NULL,
  `greason` char(1) DEFAULT NULL,
  `weightlb` varchar(10) DEFAULT NULL,
  `weightkg` varchar(10) DEFAULT NULL,
  `bp` text,
  `pulse` text,
  `heightin` varchar(10) DEFAULT NULL,
  `heightft` varchar(10) DEFAULT NULL,
  `heightmetric` varchar(10) DEFAULT NULL,
  `goodreason` text,
  `infodate` date DEFAULT NULL,
  PRIMARY KEY (`id`)
) ENGINE=InnoDB AUTO_INCREMENT=102548 DEFAULT CHARSET=utf8;
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `riskos`
--

LOCK TABLES `riskos` WRITE;
/*!40000 ALTER TABLE `riskos` DISABLE KEYS */;
INSERT INTO `riskos` VALUES ( ******* LONG LIST OF VALUES ******* );

/*!40000 ALTER TABLE `riskos` ENABLE KEYS */;
UNLOCK TABLES;

--
-- Table structure for table `sessiontracking`
--

DROP TABLE IF EXISTS `sessiontracking`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!50503 SET character_set_client = utf8mb4 */;
CREATE TABLE `sessiontracking` (
  `ID` int(11) NOT NULL AUTO_INCREMENT,
  `tstamp` timestamp NULL DEFAULT NULL,
  `sessiondump` varchar(200) DEFAULT NULL,
  PRIMARY KEY (`ID`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8;
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `sessiontracking`
--

LOCK TABLES `sessiontracking` WRITE;
/*!40000 ALTER TABLE `sessiontracking` DISABLE KEYS */;
/*!40000 ALTER TABLE `sessiontracking` ENABLE KEYS */;
UNLOCK TABLES;

--
-- Table structure for table `useractivity`
--

DROP TABLE IF EXISTS `useractivity`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!50503 SET character_set_client = utf8mb4 */;
CREATE TABLE `useractivity` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `tStamp` timestamp NULL DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP,
  `UserID` int(11) DEFAULT NULL,
  `TeamID` int(11) DEFAULT NULL,
  `pageaction` varchar(80) DEFAULT NULL,
  `controller` varchar(30) DEFAULT NULL,
  `REMOTE_ADDR` varchar(20) DEFAULT NULL,
  `role` varchar(20) DEFAULT NULL,
  PRIMARY KEY (`id`)
) ENGINE=MyISAM DEFAULT CHARSET=utf8;
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `useractivity`
--

LOCK TABLES `useractivity` WRITE;
/*!40000 ALTER TABLE `useractivity` DISABLE KEYS */;
/*!40000 ALTER TABLE `useractivity` ENABLE KEYS */;
UNLOCK TABLES;

--
-- Table structure for table `wp_commentmeta`
--

DROP TABLE IF EXISTS `wp_commentmeta`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!50503 SET character_set_client = utf8mb4 */;
CREATE TABLE `wp_commentmeta` (
  `meta_id` bigint(20) unsigned NOT NULL AUTO_INCREMENT,
  `comment_id` bigint(20) unsigned NOT NULL DEFAULT '0',
  `meta_key` varchar(255) DEFAULT NULL,
  `meta_value` longtext,
  PRIMARY KEY (`meta_id`),
  KEY `comment_id` (`comment_id`),
  KEY `meta_key` (`meta_key`(191))
) ENGINE=MyISAM AUTO_INCREMENT=5 DEFAULT CHARSET=utf8;
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `wp_commentmeta`
--

LOCK TABLES `wp_commentmeta` WRITE;
/*!40000 ALTER TABLE `wp_commentmeta` DISABLE KEYS */;
/*!40000 ALTER TABLE `wp_commentmeta` ENABLE KEYS */;
UNLOCK TABLES;

--
-- Table structure for table `wp_comments`
--

DROP TABLE IF EXISTS `wp_comments`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!50503 SET character_set_client = utf8mb4 */;
CREATE TABLE `wp_comments` (
  `comment_ID` bigint(20) unsigned NOT NULL AUTO_INCREMENT,
  `comment_post_ID` bigint(20) unsigned NOT NULL DEFAULT '0',
  `comment_author` tinytext NOT NULL,
  `comment_author_email` varchar(100) NOT NULL DEFAULT '',
  `comment_author_url` varchar(200) NOT NULL DEFAULT '',
  `comment_author_IP` varchar(100) NOT NULL DEFAULT '',
  `comment_date` datetime NOT NULL DEFAULT '0000-00-00 00:00:00',
  `comment_date_gmt` datetime NOT NULL DEFAULT '0000-00-00 00:00:00',
  `comment_content` text NOT NULL,
  `comment_karma` int(11) NOT NULL DEFAULT '0',
  `comment_approved` varchar(20) NOT NULL DEFAULT '1',
  `comment_agent` varchar(255) NOT NULL DEFAULT '',
  `comment_type` varchar(20) NOT NULL DEFAULT 'comment',
  `comment_parent` bigint(20) unsigned NOT NULL DEFAULT '0',
  `user_id` bigint(20) unsigned NOT NULL DEFAULT '0',
  PRIMARY KEY (`comment_ID`),
  KEY `comment_post_ID` (`comment_post_ID`),
  KEY `comment_approved_date_gmt` (`comment_approved`,`comment_date_gmt`),
  KEY `comment_date_gmt` (`comment_date_gmt`),
  KEY `comment_parent` (`comment_parent`),
  KEY `comment_author_email` (`comment_author_email`(10))
) ENGINE=MyISAM AUTO_INCREMENT=4 DEFAULT CHARSET=utf8;
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `wp_comments`
--

LOCK TABLES `wp_comments` WRITE;
/*!40000 ALTER TABLE `wp_comments` DISABLE KEYS */;
INSERT INTO `wp_comments` VALUES ( ******* LONG LIST OF VALUES ******* );

/*!40000 ALTER TABLE `wp_comments` ENABLE KEYS */;
UNLOCK TABLES;

--
-- Table structure for table `wp_layerslider`
--

DROP TABLE IF EXISTS `wp_layerslider`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!50503 SET character_set_client = utf8mb4 */;
CREATE TABLE `wp_layerslider` (
  `id` int(10) NOT NULL AUTO_INCREMENT,
  `author` int(10) NOT NULL DEFAULT '0',
  `name` varchar(100) NOT NULL,
  `slug` varchar(100) NOT NULL,
  `data` mediumtext NOT NULL,
  `date_c` int(10) NOT NULL,
  `date_m` int(11) NOT NULL,
  `flag_hidden` tinyint(1) NOT NULL DEFAULT '0',
  `flag_deleted` tinyint(1) NOT NULL DEFAULT '0',
  PRIMARY KEY (`id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8;
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `wp_layerslider`
--

LOCK TABLES `wp_layerslider` WRITE;
/*!40000 ALTER TABLE `wp_layerslider` DISABLE KEYS */;
/*!40000 ALTER TABLE `wp_layerslider` ENABLE KEYS */;
UNLOCK TABLES;

--
-- Table structure for table `wp_links`
--

DROP TABLE IF EXISTS `wp_links`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!50503 SET character_set_client = utf8mb4 */;
CREATE TABLE `wp_links` (
  `link_id` bigint(20) unsigned NOT NULL AUTO_INCREMENT,
  `link_url` varchar(255) NOT NULL DEFAULT '',
  `link_name` varchar(255) NOT NULL DEFAULT '',
  `link_image` varchar(255) NOT NULL DEFAULT '',
  `link_target` varchar(25) NOT NULL DEFAULT '',
  `link_description` varchar(255) NOT NULL DEFAULT '',
  `link_visible` varchar(20) NOT NULL DEFAULT 'Y',
  `link_owner` bigint(20) unsigned NOT NULL DEFAULT '1',
  `link_rating` int(11) NOT NULL DEFAULT '0',
  `link_updated` datetime NOT NULL DEFAULT '0000-00-00 00:00:00',
  `link_rel` varchar(255) NOT NULL DEFAULT '',
  `link_notes` mediumtext NOT NULL,
  `link_rss` varchar(255) NOT NULL DEFAULT '',
  PRIMARY KEY (`link_id`),
  KEY `link_visible` (`link_visible`)
) ENGINE=MyISAM DEFAULT CHARSET=utf8;
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `wp_links`
--

LOCK TABLES `wp_links` WRITE;
/*!40000 ALTER TABLE `wp_links` DISABLE KEYS */;
/*!40000 ALTER TABLE `wp_links` ENABLE KEYS */;
UNLOCK TABLES;

--
-- Table structure for table `wp_options`
--

DROP TABLE IF EXISTS `wp_options`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!50503 SET character_set_client = utf8mb4 */;
CREATE TABLE `wp_options` (
  `option_id` bigint(20) unsigned NOT NULL AUTO_INCREMENT,
  `option_name` varchar(191) DEFAULT NULL,
  `option_value` longtext NOT NULL,
  `autoload` varchar(20) NOT NULL DEFAULT 'yes',
  PRIMARY KEY (`option_id`),
  UNIQUE KEY `option_name` (`option_name`),
  KEY `autoload` (`autoload`)
) ENGINE=MyISAM AUTO_INCREMENT=144669 DEFAULT CHARSET=utf8;
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `wp_options`
--

LOCK TABLES `wp_options` WRITE;
/*!40000 ALTER TABLE `wp_options` DISABLE KEYS */;
INSERT INTO `wp_options` VALUES ( ******* LONG LIST OF VALUES ******* );

/*!40000 ALTER TABLE `wp_options` ENABLE KEYS */;
UNLOCK TABLES;

--
-- Table structure for table `wp_postmeta`
--

DROP TABLE IF EXISTS `wp_postmeta`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!50503 SET character_set_client = utf8mb4 */;
CREATE TABLE `wp_postmeta` (
  `meta_id` bigint(20) unsigned NOT NULL AUTO_INCREMENT,
  `post_id` bigint(20) unsigned NOT NULL DEFAULT '0',
  `meta_key` varchar(255) DEFAULT NULL,
  `meta_value` longtext,
  PRIMARY KEY (`meta_id`),
  KEY `post_id` (`post_id`),
  KEY `meta_key` (`meta_key`(191))
) ENGINE=MyISAM AUTO_INCREMENT=5160 DEFAULT CHARSET=utf8;
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `wp_postmeta`
--

LOCK TABLES `wp_postmeta` WRITE;
/*!40000 ALTER TABLE `wp_postmeta` DISABLE KEYS */;
INSERT INTO `wp_postmeta` VALUES ( ******* LONG LIST OF VALUES ******* );

/*!40000 ALTER TABLE `wp_postmeta` ENABLE KEYS */;
UNLOCK TABLES;

--
-- Table structure for table `wp_posts`
--

DROP TABLE IF EXISTS `wp_posts`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!50503 SET character_set_client = utf8mb4 */;
CREATE TABLE `wp_posts` (
  `ID` bigint(20) unsigned NOT NULL AUTO_INCREMENT,
  `post_author` bigint(20) unsigned NOT NULL DEFAULT '0',
  `post_date` datetime NOT NULL DEFAULT '0000-00-00 00:00:00',
  `post_date_gmt` datetime NOT NULL DEFAULT '0000-00-00 00:00:00',
  `post_content` longtext NOT NULL,
  `post_title` text NOT NULL,
  `post_excerpt` text NOT NULL,
  `post_status` varchar(20) NOT NULL DEFAULT 'publish',
  `comment_status` varchar(20) NOT NULL DEFAULT 'open',
  `ping_status` varchar(20) NOT NULL DEFAULT 'open',
  `post_password` varchar(255) NOT NULL DEFAULT '',
  `post_name` varchar(200) NOT NULL DEFAULT '',
  `to_ping` text NOT NULL,
  `pinged` text NOT NULL,
  `post_modified` datetime NOT NULL DEFAULT '0000-00-00 00:00:00',
  `post_modified_gmt` datetime NOT NULL DEFAULT '0000-00-00 00:00:00',
  `post_content_filtered` longtext NOT NULL,
  `post_parent` bigint(20) unsigned NOT NULL DEFAULT '0',
  `guid` varchar(255) NOT NULL DEFAULT '',
  `menu_order` int(11) NOT NULL DEFAULT '0',
  `post_type` varchar(20) NOT NULL DEFAULT 'post',
  `post_mime_type` varchar(100) NOT NULL DEFAULT '',
  `comment_count` bigint(20) NOT NULL DEFAULT '0',
  PRIMARY KEY (`ID`),
  KEY `type_status_date` (`post_type`,`post_status`,`post_date`,`ID`),
  KEY `post_parent` (`post_parent`),
  KEY `post_author` (`post_author`),
  KEY `post_name` (`post_name`(191))
) ENGINE=MyISAM AUTO_INCREMENT=8413 DEFAULT CHARSET=utf8;
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `wp_posts`
--

LOCK TABLES `wp_posts` WRITE;
/*!40000 ALTER TABLE `wp_posts` DISABLE KEYS */;
INSERT INTO `wp_posts` VALUES ( ******* LONG LIST OF VALUES ******* );

/*!40000 ALTER TABLE `wp_posts` ENABLE KEYS */;
UNLOCK TABLES;

--
-- Table structure for table `wp_revslider_css`
--

DROP TABLE IF EXISTS `wp_revslider_css`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!50503 SET character_set_client = utf8mb4 */;
CREATE TABLE `wp_revslider_css` (
  `id` int(9) NOT NULL AUTO_INCREMENT,
  `handle` text NOT NULL,
  `settings` longtext,
  `hover` longtext,
  `params` longtext NOT NULL,
  `advanced` longtext,
  UNIQUE KEY `id` (`id`)
) ENGINE=InnoDB AUTO_INCREMENT=110 DEFAULT CHARSET=latin1;
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `wp_revslider_css`
--

LOCK TABLES `wp_revslider_css` WRITE;
/*!40000 ALTER TABLE `wp_revslider_css` DISABLE KEYS */;
INSERT INTO `wp_revslider_css` VALUES ( ******* LONG LIST OF VALUES ******* );

/*!40000 ALTER TABLE `wp_term_relationships` ENABLE KEYS */;
UNLOCK TABLES;

--
-- Table structure for table `wp_term_taxonomy`
--

DROP TABLE IF EXISTS `wp_term_taxonomy`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!50503 SET character_set_client = utf8mb4 */;
CREATE TABLE `wp_term_taxonomy` (
  `term_taxonomy_id` bigint(20) unsigned NOT NULL AUTO_INCREMENT,
  `term_id` bigint(20) unsigned NOT NULL DEFAULT '0',
  `taxonomy` varchar(32) NOT NULL DEFAULT '',
  `description` longtext NOT NULL,
  `parent` bigint(20) unsigned NOT NULL DEFAULT '0',
  `count` bigint(20) NOT NULL DEFAULT '0',
  PRIMARY KEY (`term_taxonomy_id`),
  UNIQUE KEY `term_id_taxonomy` (`term_id`,`taxonomy`),
  KEY `taxonomy` (`taxonomy`)
) ENGINE=MyISAM AUTO_INCREMENT=22 DEFAULT CHARSET=utf8;
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `wp_term_taxonomy`
--

LOCK TABLES `wp_term_taxonomy` WRITE;
/*!40000 ALTER TABLE `wp_term_taxonomy` DISABLE KEYS */;
INSERT INTO `wp_term_taxonomy` VALUES ( ******* LONG LIST OF VALUES ******* );

/*!40000 ALTER TABLE `wp_term_taxonomy` ENABLE KEYS */;
UNLOCK TABLES;

--
-- Table structure for table `wp_termmeta`
--

DROP TABLE IF EXISTS `wp_termmeta`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!50503 SET character_set_client = utf8mb4 */;
CREATE TABLE `wp_termmeta` (
  `meta_id` bigint(20) unsigned NOT NULL AUTO_INCREMENT,
  `term_id` bigint(20) unsigned NOT NULL DEFAULT '0',
  `meta_key` varchar(255) DEFAULT NULL,
  `meta_value` longtext,
  PRIMARY KEY (`meta_id`),
  KEY `term_id` (`term_id`),
  KEY `meta_key` (`meta_key`(191))
) ENGINE=InnoDB DEFAULT CHARSET=utf8;
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `wp_termmeta`
--

LOCK TABLES `wp_termmeta` WRITE;
/*!40000 ALTER TABLE `wp_termmeta` DISABLE KEYS */;
/*!40000 ALTER TABLE `wp_termmeta` ENABLE KEYS */;
UNLOCK TABLES;

--
-- Table structure for table `wp_terms`
--

DROP TABLE IF EXISTS `wp_terms`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!50503 SET character_set_client = utf8mb4 */;
CREATE TABLE `wp_terms` (
  `term_id` bigint(20) unsigned NOT NULL AUTO_INCREMENT,
  `name` varchar(200) NOT NULL DEFAULT '',
  `slug` varchar(200) NOT NULL DEFAULT '',
  `term_group` bigint(10) NOT NULL DEFAULT '0',
  PRIMARY KEY (`term_id`),
  KEY `slug` (`slug`(191)),
  KEY `name` (`name`(191))
) ENGINE=MyISAM AUTO_INCREMENT=22 DEFAULT CHARSET=utf8;
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `wp_terms`
--

LOCK TABLES `wp_terms` WRITE;
/*!40000 ALTER TABLE `wp_terms` DISABLE KEYS */;
INSERT INTO `wp_terms` VALUES ( ******* LONG LIST OF VALUES ******* );

/*!40000 ALTER TABLE `wp_terms` ENABLE KEYS */;
UNLOCK TABLES;

--
-- Table structure for table `wp_usermeta`
--

DROP TABLE IF EXISTS `wp_usermeta`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!50503 SET character_set_client = utf8mb4 */;
CREATE TABLE `wp_usermeta` (
  `umeta_id` bigint(20) unsigned NOT NULL AUTO_INCREMENT,
  `user_id` bigint(20) unsigned NOT NULL DEFAULT '0',
  `meta_key` varchar(255) DEFAULT NULL,
  `meta_value` longtext,
  PRIMARY KEY (`umeta_id`),
  KEY `user_id` (`user_id`),
  KEY `meta_key` (`meta_key`(191))
) ENGINE=MyISAM AUTO_INCREMENT=558 DEFAULT CHARSET=utf8;
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `wp_usermeta`
--

LOCK TABLES `wp_usermeta` WRITE;
/*!40000 ALTER TABLE `wp_usermeta` DISABLE KEYS */;
INSERT INTO `wp_usermeta` VALUES ( ******* LONG LIST OF VALUES ******* );

/*!40000 ALTER TABLE `wp_usermeta` ENABLE KEYS */;
UNLOCK TABLES;

--
-- Table structure for table `wp_users`
--

DROP TABLE IF EXISTS `wp_users`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!50503 SET character_set_client = utf8mb4 */;
CREATE TABLE `wp_users` (
  `ID` bigint(20) unsigned NOT NULL AUTO_INCREMENT,
  `user_login` varchar(60) NOT NULL DEFAULT '',
  `user_pass` varchar(255) NOT NULL DEFAULT '',
  `user_nicename` varchar(50) NOT NULL DEFAULT '',
  `user_email` varchar(100) NOT NULL DEFAULT '',
  `user_url` varchar(100) NOT NULL DEFAULT '',
  `user_registered` datetime NOT NULL DEFAULT '0000-00-00 00:00:00',
  `user_activation_key` varchar(255) NOT NULL DEFAULT '',
  `user_status` int(11) NOT NULL DEFAULT '0',
  `display_name` varchar(250) NOT NULL DEFAULT '',
  PRIMARY KEY (`ID`),
  KEY `user_login_key` (`user_login`),
  KEY `user_nicename` (`user_nicename`),
  KEY `user_email` (`user_email`)
) ENGINE=MyISAM AUTO_INCREMENT=6 DEFAULT CHARSET=utf8;
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `wp_users`
--

LOCK TABLES `wp_users` WRITE;
/*!40000 ALTER TABLE `wp_users` DISABLE KEYS */;
INSERT INTO `wp_users` VALUES ( ******* LONG LIST OF VALUES ******* );

/*!40000 ALTER TABLE `wp_users` ENABLE KEYS */;
UNLOCK TABLES;

--
-- Table structure for table `wptg_tables`
--

DROP TABLE IF EXISTS `wptg_tables`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!50503 SET character_set_client = utf8mb4 */;
CREATE TABLE `wptg_tables` (
  `id` mediumint(9) NOT NULL AUTO_INCREMENT,
  `name` tinytext NOT NULL,
  `rows` mediumint(9) NOT NULL,
  `cols` mediumint(9) NOT NULL,
  `tvalues` longtext NOT NULL,
  UNIQUE KEY `id` (`id`)
) ENGINE=InnoDB AUTO_INCREMENT=3 DEFAULT CHARSET=latin1;
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `wptg_tables`
--

LOCK TABLES `wptg_tables` WRITE;
/*!40000 ALTER TABLE `wptg_tables` DISABLE KEYS */;
INSERT INTO `wptg_tables` VALUES ( ******* LONG LIST OF VALUES ******* );

/*!40000 ALTER TABLE `wptg_tables` ENABLE KEYS */;
UNLOCK TABLES;
/*!40103 SET TIME_ZONE=@OLD_TIME_ZONE */;

/*!40101 SET SQL_MODE=@OLD_SQL_MODE */;
/*!40014 SET FOREIGN_KEY_CHECKS=@OLD_FOREIGN_KEY_CHECKS */;
/*!40014 SET UNIQUE_CHECKS=@OLD_UNIQUE_CHECKS */;
/*!40101 SET CHARACTER_SET_CLIENT=@OLD_CHARACTER_SET_CLIENT */;
/*!40101 SET CHARACTER_SET_RESULTS=@OLD_CHARACTER_SET_RESULTS */;
/*!40101 SET COLLATION_CONNECTION=@OLD_COLLATION_CONNECTION */;
/*!40111 SET SQL_NOTES=@OLD_SQL_NOTES */;

-- Dump completed on 2024-11-05 14:30:04