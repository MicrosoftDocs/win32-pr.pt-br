---
title: Classe Print-Queue
description: Contém informações sobre uma fila de impressão.
ms.assetid: 779eb37c-f94e-472a-9551-8a0f72fe0e2b
ms.tgt_platform: multiple
keywords:
- Esquema de AD de classe de Print-Queue
- Esquema do AD da classe printQueue
topic_type:
- apiref
api_name:
- Print-Queue
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ecd05290bcac514607fa44370871d1ba94b5d2b89769d9da20b91c202deea760
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753036"
---
# <a name="print-queue-class"></a>Classe Print-Queue

Contém informações sobre uma fila de impressão.



| Entrada | Valor |
|-------------------|--------------------------------------|
| CN                | Print-Queue                          |
| LDAP-Display-Name | printQueue                           |
| Privilégio de atualização  | Qualquer pessoa pode atualizar este objeto.       |
| Frequência de atualização  | \-                                   |
| Schema-ID-GUID    | bf967aa8-0de6-11d0-a285-00aa003049e2 |



## <a name="implementations"></a>Implementações

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server

-   [Atributos](#windows-2000-server-attributes)



| Entrada | Valor |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                                                                                                |
| Object-Category             | 1                                                                                                                                                                    |
| Categoria de objeto-padrão     | \-                                                                                                                                                                   |
| Governs-Id                  | 1.2.840.113556.1.5.23                                                                                                                                                |
| Padrão-ocultando valor        | 0                                                                                                                                                                    |
| RDN-ATT-ID                  | [**Nome comum**](a-cn.md)<br/>                                                                                                                               |
| Subclasse de                 | [**Ponto de conexão**](c-connectionpoint.md)<br/>                                                                                                             |
| Superiores possíveis          | Domínio do [**contêiner**](c-container.md)do [**computador**](c-computer.md)[**-**](c-domaindns.md)[**unidade organizacional**](c-organizationalunit.md) do DNS                   |
| Classes Auxiliares           | \-                                                                                                                                                                   |
| NT-Security-Descriptor      | O:BAG: INADEQUADO: S:                                                                                                                                                         |
| Descritor de segurança padrão | D: (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; PO) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; CO) (A;; RPLCLORC;;; AU |
| System-Flags                | 0x00000010                                                                                                                                                           |



## <a name="windows-2000-server-attributes"></a>Windows atributos do servidor 2000

essa classe contém os seguintes atributos para Windows servidor 2000:



| Atributo                                                                 | Obrigatório | Derivado de                                                                             |
|---------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------|
| [**Descrição do administrador**](a-admindescription.md)                           | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Administração – nome de exibição**](a-admindisplayname.md)                          | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Atributos permitidos**](a-allowedattributes.md)                         | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Permitido-atributos-efetivos**](a-allowedattributeseffective.md)      | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Classes filho permitidas**](a-allowedchildclasses.md)                    | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Permitido-filho-classes-efetivas**](a-allowedchildclasseseffective.md) | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Número de ativos**](a-assetnumber.md)                                     | Falso     | **Fila de impressão**                                                                          |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)             | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Bytes por minuto**](a-bytesperminute.md)                              | Falso     | **Fila de impressão**                                                                          |
| [**Nome canônico**](a-canonicalname.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Nome comum**](a-cn.md)                                               | Verdadeiro      | [**Ponto de conexão**](c-connectionpoint.md)<br/> [**Início**](c-top.md)<br/> |
| [**Criação-carimbo de data/hora**](a-createtimestamp.md)                            | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Prioridade padrão**](a-defaultpriority.md)                             | Falso     | **Fila de impressão**                                                                          |
| [**Descrição**](a-description.md)                                      | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Nome de exibição**](a-displayname.md)                                     | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Nome de exibição imprimível**](a-displaynameprintable.md)                  | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Nome do driver**](a-drivername.md)                                       | Falso     | **Fila de Impressão**                                                                          |
| [**Versão do driver**](a-driverversion.md)                                 | Falso     | **Fila de Impressão**                                                                          |
| [**Assinatura DSA**](a-dsasignature.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)               | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Nome da extensão**](a-extensionname.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Sinalizadores**](a-flags.md)                                                  | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Entrada de entrada**](a-fromentry.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)             | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                 | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Tipo de instância**](a-instancetype.md)                                   | Verdadeiro      | [**Início**](c-top.md)<br/>                                                          |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)             | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Is-Deleted**](a-isdeleted.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Is-Member-of-DL**](a-memberof.md)                                     | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                        | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Palavras-chave**](a-keywords.md)                                            | Falso     | [**Ponto de conexão**](c-connectionpoint.md)<br/>                                 |
| [**Último pai conhecido**](a-lastknownparent.md)                            | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Local**](a-location.md)                                            | Falso     | **Fila de Impressão**                                                                          |
| [**Gerenciado por**](a-managedby.md)                                         | Falso     | [**Ponto de conexão**](c-connectionpoint.md)<br/>                                 |
| [**Objetos gerenciados**](a-managedobjects.md)                               | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Mastered-By**](a-masteredby.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Modificar carimbo de data/hora**](a-modifytimestamp.md)                            | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)    | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                 | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                  | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                   | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Descritor de segurança NT**](a-ntsecuritydescriptor.md)                  | Verdadeiro      | [**Início**](c-top.md)<br/>                                                          |
| [**Obj-Dist-Name**](a-distinguishedname.md)                              | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Categoria de objeto**](a-objectcategory.md)                               | Verdadeiro      | [**Início**](c-top.md)<br/>                                                          |
| [**Classe de objeto**](a-objectclass.md)                                     | Verdadeiro      | [**Início**](c-top.md)<br/>                                                          |
| [**Guid de objeto**](a-objectguid.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Versão do objeto**](a-objectversion.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Sistema operacional**](a-operatingsystem.md)                             | Falso     | **Fila de Impressão**                                                                          |
| [**Hotfix do sistema operacional**](a-operatingsystemhotfix.md)                | Falso     | **Fila de Impressão**                                                                          |
| [**Operating-System-Service-Pack**](a-operatingsystemservicepack.md)     | Falso     | **Fila de Impressão**                                                                          |
| [**Versão do sistema operacional**](a-operatingsystemversion.md)              | Falso     | **Fila de Impressão**                                                                          |
| [**Outros objetos conhecidos**](a-otherwellknownobjects.md)               | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md) | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Conjunto de atributos parcial**](a-partialattributeset.md)                    | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Physical-Location-Object**](a-physicallocationobject.md)              | Falso     | **Fila de Impressão**                                                                          |
| [**Nome da porta**](a-portname.md)                                           | Falso     | **Fila de Impressão**                                                                          |
| [**Possíveis inferiores**](a-possibleinferiors.md)                         | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Atributos de impressão**](a-printattributes.md)                             | Falso     | **Fila de Impressão**                                                                          |
| [**Nomes de compartimento de impressão**](a-printbinnames.md)                                | Falso     | **Fila de Impressão**                                                                          |
| [**Print-Collate**](a-printcollate.md)                                   | Falso     | **Fila de Impressão**                                                                          |
| [**Cor da impressão**](a-printcolor.md)                                       | Falso     | **Fila de Impressão**                                                                          |
| [**Com suporte para Print-Duplex**](a-printduplexsupported.md)                  | Falso     | **Fila de Impressão**                                                                          |
| [**Hora de término da impressão**](a-printendtime.md)                                  | Falso     | **Fila de Impressão**                                                                          |
| [**Nome da impressora**](a-printername.md)                                     | Verdadeiro      | **Fila de Impressão**                                                                          |
| [**Imprimir o nome do formulário**](a-printformname.md)                                | Falso     | **Fila de Impressão**                                                                          |
| [**Print-Keep-Printed-Jobs**](a-printkeepprintedjobs.md)                 | Falso     | **Fila de Impressão**                                                                          |
| [**Linguagem de impressão**](a-printlanguage.md)                                 | Falso     | **Fila de Impressão**                                                                          |
| [**Print-MAC-Address**](a-printmacaddress.md)                            | Falso     | **Fila de Impressão**                                                                          |
| [**Print-Max-Copies**](a-printmaxcopies.md)                              | Falso     | **Fila de Impressão**                                                                          |
| [**Print-Max-Resolution-Supported**](a-printmaxresolutionsupported.md)   | Falso     | **Fila de Impressão**                                                                          |
| [**Extensão Print-Max-X**](a-printmaxxextent.md)                           | Falso     | **Fila de Impressão**                                                                          |
| [**Extensão print-max-y**](a-printmaxyextent.md)                           | Falso     | **Fila de Impressão**                                                                          |
| [**Print-Media-Ready**](a-printmediaready.md)                            | Falso     | **Fila de Impressão**                                                                          |
| [**Com suporte para mídia de impressão**](a-printmediasupported.md)                    | Falso     | **Fila de Impressão**                                                                          |
| [**Memória de impressão**](a-printmemory.md)                                     | Falso     | **Fila de Impressão**                                                                          |
| [**Extensão Print-Min-X**](a-printminxextent.md)                           | Falso     | **Fila de Impressão**                                                                          |
| [**Extensão print-min-y**](a-printminyextent.md)                           | Falso     | **Fila de Impressão**                                                                          |
| [**Print-Network-Address**](a-printnetworkaddress.md)                    | Falso     | **Fila de Impressão**                                                                          |
| [**Notificação de impressão**](a-printnotify.md)                                     | Falso     | **Fila de Impressão**                                                                          |
| [**Número de impressão**](a-printnumberup.md)                                | Falso     | **Fila de Impressão**                                                                          |
| [**Orientação de impressão com suporte**](a-printorientationssupported.md)      | Falso     | **Fila de Impressão**                                                                          |
| [**Print-Owner**](a-printowner.md)                                       | Falso     | **Fila de Impressão**                                                                          |
| [**Imprimir páginas por minuto**](a-printpagesperminute.md)                   | Falso     | **Fila de Impressão**                                                                          |
| [**Taxa de impressão**](a-printrate.md)                                         | Falso     | **Fila de Impressão**                                                                          |
| [**Unidade de taxa de impressão**](a-printrateunit.md)                                | Falso     | **Fila de Impressão**                                                                          |
| [**Print-Separator-File**](a-printseparatorfile.md)                      | Falso     | **Fila de Impressão**                                                                          |
| [**Print-Share-Name**](a-printsharename.md)                              | Falso     | **Fila de Impressão**                                                                          |
| [**Spooling de impressão**](a-printspooling.md)                                 | Falso     | **Fila de Impressão**                                                                          |
| [**Com suporte para print-stapling**](a-printstaplingsupported.md)              | Falso     | **Fila de Impressão**                                                                          |
| [**Print-Start-Time**](a-printstarttime.md)                              | Falso     | **Fila de Impressão**                                                                          |
| [**Print-Status**](a-printstatus.md)                                     | Falso     | **Fila de Impressão**                                                                          |
| [**Priority**](a-priority.md)                                            | Falso     | **Fila de Impressão**                                                                          |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                        | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Endereços proxy**](a-proxyaddresses.md)                               | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Query-Policy-BL**](a-querypolicybl.md)                                | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Rdn**](a-name.md)                                                     | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                 | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                      | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Relatórios**](a-directreports.md)                                        | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Reps-From**](a-repsfrom.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Reps-To**](a-repsto.md)                                               | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Revisão**](a-revision.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                        | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Nome do servidor**](a-servername.md)                                       | Verdadeiro      | **Fila de Impressão**                                                                          |
| [**Server-Reference-BL**](a-serverreferencebl.md)                        | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Nome curto do servidor**](a-shortservername.md)                            | Verdadeiro      | **Fila de Impressão**                                                                          |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)            | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Site-Object-BL**](a-siteobjectbl.md)                                  | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Sub-refs**](a-subrefs.md)                                             | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                          | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Sinalizadores de sistema**](a-systemflags.md)                                     | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Unc-Name**](a-uncname.md)                                             | Verdadeiro      | **Fila de Impressão**                                                                          |
| [**USN alterado**](a-usnchanged.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Criado por USN**](a-usncreated.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**UsN-Intersite**](a-usnintersite.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                               | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**USN-Source**](a-usnsource.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Número de versão**](a-versionnumber.md)                                 | Verdadeiro      | **Fila de Impressão**                                                                          |
| [**Wbem-Path**](a-wbempath.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Objetos conhecidos**](a-wellknownobjects.md)                          | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Quando alterado**](a-whenchanged.md)                                     | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Quando criado**](a-whencreated.md)                                     | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**WWW-Home Page**](a-wwwhomepage.md)                                    | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**WWW-Page-Other**](a-url.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                                          |



## <a name="windows-server-2003"></a>Windows Server 2003

-   [Atributos](#windows-server-2003-attributes)



| Entrada | Valor |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                                                                                                |
| Object-Category             | 1                                                                                                                                                                    |
| Default-Object-Category     | \-                                                                                                                                                                   |
| Governs-Id                  | 1.2.840.113556.1.5.23                                                                                                                                                |
| Valor ocultado padrão        | 0                                                                                                                                                                    |
| Rdn-Att-Id                  | [**Common-Name**](a-cn.md)<br/>                                                                                                                               |
| Subclasse de                 | [**Ponto de conexão**](c-connectionpoint.md)<br/>                                                                                                             |
| Possíveis superiores          | [**Unidade**](c-computer.md)[**organizacional**](c-container.md)[**dns-de-domínio do contêiner**](c-domaindns.md)do [**computador**](c-organizationalunit.md)                   |
| Classes Auxiliares           | \-                                                                                                                                                                   |
| Descritor de segurança NT      | O:BAG:BAD:S:                                                                                                                                                         |
| Descritor de segurança padrão | D:(A;; RPWPCRCCDCLCLORCWOWDSDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDTSW;;; SY)(A;; RPWPCRCCDCLCLORCWOWDSDTSW;;; PO)(A;; RPWPCRCCDCLCLORCWOWDSDTSW;;; CO)(A;; RPLCLORC;;; AU) |
| System-Flags                | 0x00000010                                                                                                                                                           |



## <a name="windows-server-2003-attributes"></a>Windows Atributos do Server 2003

Essa classe contém os seguintes atributos para Windows Server 2003:



| Atributo                                                                   | Obrigatório | Derivado de                                                                             |
|-----------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------|
| [**Descrição do administrador**](a-admindescription.md)                             | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Admin-Display-Name**](a-admindisplayname.md)                            | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Atributos permitidos**](a-allowedattributes.md)                           | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)        | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Classes filho permitidas**](a-allowedchildclasses.md)                      | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)   | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Número do ativo**](a-assetnumber.md)                                       | Falso     | **Fila de Impressão**                                                                          |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)               | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Bytes por minuto**](a-bytesperminute.md)                                | Falso     | **Fila de Impressão**                                                                          |
| [**Nome canônico**](a-canonicalname.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Common-Name**](a-cn.md)                                                 | Verdadeiro      | [**Ponto de conexão**](c-connectionpoint.md)<br/> [**Início**](c-top.md)<br/> |
| [**Criar carimbo de data/hora**](a-createtimestamp.md)                              | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Prioridade padrão**](a-defaultpriority.md)                               | Falso     | **Fila de impressão**                                                                          |
| [**Descrição**](a-description.md)                                        | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Nome de exibição**](a-displayname.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Nome de exibição-imprimível**](a-displaynameprintable.md)                    | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Nome do driver**](a-drivername.md)                                         | Falso     | **Fila de impressão**                                                                          |
| [**Versão do driver**](a-driverversion.md)                                   | Falso     | **Fila de impressão**                                                                          |
| [**DSA-assinatura**](a-dsasignature.md)                                     | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**DS-Core-propagação-data**](a-dscorepropagationdata.md)                 | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Nome da extensão**](a-extensionname.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Flags**](a-flags.md)                                                    | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**De entrada**](a-fromentry.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**FRS-member-Reference-BL**](a-frsmemberreferencebl.md)                   | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**FSMO-função-proprietário**](a-fsmoroleowner.md)                                  | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Tipo de instância**](a-instancetype.md)                                     | Verdadeiro      | [**Início**](c-top.md)<br/>                                                          |
| [**É-crítico-System-Object**](a-iscriticalsystemobject.md)               | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**É excluído**](a-isdeleted.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Is-member-of-DL**](a-memberof.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**É com proprietário de privilégio**](a-isprivilegeholder.md)                          | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Palavras-chave**](a-keywords.md)                                              | Falso     | [**Ponto de conexão**](c-connectionpoint.md)<br/>                                 |
| [**Último-pai conhecido**](a-lastknownparent.md)                              | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Local**](a-location.md)                                              | Falso     | **Fila de impressão**                                                                          |
| [**Gerenciado por**](a-managedby.md)                                           | Falso     | [**Ponto de conexão**](c-connectionpoint.md)<br/>                                 |
| [**Objetos gerenciados**](a-managedobjects.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Mestre por**](a-masteredby.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Modificar-carimbo de data/hora**](a-modifytimestamp.md)                              | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                 | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**MS-COM-userlink**](a-mscom-userlink.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-aprox-immed-subordinados**](a-msds-approx-immed-subordinates.md) | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**MS-DS-Consistency-filho-Count**](a-ms-ds-consistencychildcount.md)      | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-Masterd-by**](a-msds-masteredby.md)                              | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-Members-for-AZ-role-BL**](a-msds-membersforazrolebl.md)           | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                       | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)    | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)  | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                         | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)               | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)     | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)     | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)      | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)              | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-Configurações**](a-msds-settings.md)                                   | Falso     | [**Ponto de conexão**](c-connectionpoint.md)<br/>                                 |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)               | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)               | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                    | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                     | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Descritor de segurança NT**](a-ntsecuritydescriptor.md)                    | Verdadeiro      | [**Início**](c-top.md)<br/>                                                          |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Categoria de objeto**](a-objectcategory.md)                                 | Verdadeiro      | [**Início**](c-top.md)<br/>                                                          |
| [**Classe de objeto**](a-objectclass.md)                                       | Verdadeiro      | [**Início**](c-top.md)<br/>                                                          |
| [**Guid de objeto**](a-objectguid.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Versão do objeto**](a-objectversion.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Sistema operacional**](a-operatingsystem.md)                               | Falso     | **Fila de Impressão**                                                                          |
| [**Hotfix do sistema operacional**](a-operatingsystemhotfix.md)                  | Falso     | **Fila de Impressão**                                                                          |
| [**Operating-System-Service-Pack**](a-operatingsystemservicepack.md)       | Falso     | **Fila de Impressão**                                                                          |
| [**Versão do sistema operacional**](a-operatingsystemversion.md)                | Falso     | **Fila de Impressão**                                                                          |
| [**Outros objetos conhecidos**](a-otherwellknownobjects.md)                 | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)   | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Conjunto de atributos parcial**](a-partialattributeset.md)                      | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Physical-Location-Object**](a-physicallocationobject.md)                | Falso     | **Fila de Impressão**                                                                          |
| [**Nome da porta**](a-portname.md)                                             | Falso     | **Fila de Impressão**                                                                          |
| [**Possíveis inferiores**](a-possibleinferiors.md)                           | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Atributos de impressão**](a-printattributes.md)                               | Falso     | **Fila de Impressão**                                                                          |
| [**Nomes de compartimento de impressão**](a-printbinnames.md)                                  | Falso     | **Fila de Impressão**                                                                          |
| [**Imprimir-agrupar**](a-printcollate.md)                                     | Falso     | **Fila de impressão**                                                                          |
| [**Cor de impressão**](a-printcolor.md)                                         | Falso     | **Fila de impressão**                                                                          |
| [**Impressão-duplex-com suporte**](a-printduplexsupported.md)                    | Falso     | **Fila de impressão**                                                                          |
| [**Impressão – hora de término**](a-printendtime.md)                                    | Falso     | **Fila de impressão**                                                                          |
| [**Nome da impressora**](a-printername.md)                                       | Verdadeiro      | **Fila de impressão**                                                                          |
| [**Nome do formulário de impressão**](a-printformname.md)                                  | Falso     | **Fila de impressão**                                                                          |
| [**Imprimir-manter-impresso-trabalhos**](a-printkeepprintedjobs.md)                   | Falso     | **Fila de impressão**                                                                          |
| [**Idioma de impressão**](a-printlanguage.md)                                   | Falso     | **Fila de impressão**                                                                          |
| [**Imprimir-MAC-address**](a-printmacaddress.md)                              | Falso     | **Fila de impressão**                                                                          |
| [**Imprimir-Max-cópias**](a-printmaxcopies.md)                                | Falso     | **Fila de impressão**                                                                          |
| [**Impressão-Max-resolução-com suporte**](a-printmaxresolutionsupported.md)     | Falso     | **Fila de impressão**                                                                          |
| [**Impressão-Max-X-extensão**](a-printmaxxextent.md)                             | Falso     | **Fila de impressão**                                                                          |
| [**Impressão-Max-Y-extensão**](a-printmaxyextent.md)                             | Falso     | **Fila de impressão**                                                                          |
| [**Impressão-mídia pronta**](a-printmediaready.md)                              | Falso     | **Fila de impressão**                                                                          |
| [**Impressão-mídia-com suporte**](a-printmediasupported.md)                      | Falso     | **Fila de impressão**                                                                          |
| [**Memória de impressão**](a-printmemory.md)                                       | Falso     | **Fila de impressão**                                                                          |
| [**Impressão-min-X-extensão**](a-printminxextent.md)                             | Falso     | **Fila de impressão**                                                                          |
| [**Impressão-min-Y-extensão**](a-printminyextent.md)                             | Falso     | **Fila de impressão**                                                                          |
| [**Endereço de rede de impressão**](a-printnetworkaddress.md)                      | Falso     | **Fila de impressão**                                                                          |
| [**Imprimir-notificar**](a-printnotify.md)                                       | Falso     | **Fila de impressão**                                                                          |
| [**Imprimir-numeração**](a-printnumberup.md)                                  | Falso     | **Fila de impressão**                                                                          |
| [**Orientações de impressão-com suporte**](a-printorientationssupported.md)        | Falso     | **Fila de impressão**                                                                          |
| [**Imprimir-proprietário**](a-printowner.md)                                         | Falso     | **Fila de impressão**                                                                          |
| [**Imprimir páginas por minuto**](a-printpagesperminute.md)                     | Falso     | **Fila de impressão**                                                                          |
| [**Taxa de impressão**](a-printrate.md)                                           | Falso     | **Fila de impressão**                                                                          |
| [**Unidade de taxa de impressão**](a-printrateunit.md)                                  | Falso     | **Fila de impressão**                                                                          |
| [**Imprimir-separador de arquivo**](a-printseparatorfile.md)                        | Falso     | **Fila de impressão**                                                                          |
| [**Nome de compartilhamento de impressão**](a-printsharename.md)                                | Falso     | **Fila de impressão**                                                                          |
| [**Spool de impressão**](a-printspooling.md)                                   | Falso     | **Fila de impressão**                                                                          |
| [**Grampeamento de impressão-com suporte**](a-printstaplingsupported.md)                | Falso     | **Fila de impressão**                                                                          |
| [**Imprimir-hora de início**](a-printstarttime.md)                                | Falso     | **Fila de impressão**                                                                          |
| [**Status de impressão**](a-printstatus.md)                                       | Falso     | **Fila de impressão**                                                                          |
| [**Priority**](a-priority.md)                                              | Falso     | **Fila de impressão**                                                                          |
| [**Nome-do-objeto-proxy**](a-proxiedobjectname.md)                          | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Endereços de proxy**](a-proxyaddresses.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Consulta-política-BL**](a-querypolicybl.md)                                  | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**RDN**](a-name.md)                                                       | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Repl-Property-meta-data**](a-replpropertymetadata.md)                   | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Repl-UpToDate-vector**](a-repluptodatevector.md)                        | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Relatórios**](a-directreports.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Representantes-de**](a-repsfrom.md)                                             | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Reps-to**](a-repsto.md)                                                 | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Revisão**](a-revision.md)                                              | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**SD-direitos-efetivos**](a-sdrightseffective.md)                          | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Nome do servidor**](a-servername.md)                                         | Verdadeiro      | **Fila de impressão**                                                                          |
| [**Servidor-referência-BL**](a-serverreferencebl.md)                          | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Nome de servidor curto**](a-shortservername.md)                              | Verdadeiro      | **Fila de impressão**                                                                          |
| [**Mostrar-in-avançado-somente exibição**](a-showinadvancedviewonly.md)              | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Classe de objeto estrutural**](a-structuralobjectclass.md)                  | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Sub-referências**](a-subrefs.md)                                               | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Sinalizadores do sistema**](a-systemflags.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Nome UNC**](a-uncname.md)                                               | Verdadeiro      | **Fila de impressão**                                                                          |
| [**USN-alterado**](a-usnchanged.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Criado pelo USN**](a-usncreated.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**USN-DSA-Last-obj-removido**](a-usndsalastobjremoved.md)                  | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**USN-entre sites**](a-usnintersite.md)                                     | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**USN-fonte**](a-usnsource.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Número de versão**](a-versionnumber.md)                                   | Verdadeiro      | **Fila de impressão**                                                                          |
| [**WBEM-caminho**](a-wbempath.md)                                             | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Objetos bem conhecidos**](a-wellknownobjects.md)                            | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Quando-alterado**](a-whenchanged.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Quando-criado**](a-whencreated.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**WWW-Home-Page**](a-wwwhomepage.md)                                      | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**WWW-página-outro**](a-url.md)                                             | Falso     | [**Início**](c-top.md)<br/>                                                          |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2

-   [Atributos](#windows-server-2003-r2-attributes)



| Entrada | Valor |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                                                                                                |
| Object-Category             | 1                                                                                                                                                                    |
| Categoria de objeto-padrão     | \-                                                                                                                                                                   |
| Governs-Id                  | 1.2.840.113556.1.5.23                                                                                                                                                |
| Padrão-ocultando valor        | 0                                                                                                                                                                    |
| RDN-ATT-ID                  | [**Nome comum**](a-cn.md)<br/>                                                                                                                               |
| Subclasse de                 | [**Ponto de conexão**](c-connectionpoint.md)<br/>                                                                                                             |
| Superiores possíveis          | Domínio do [**contêiner**](c-container.md)do [**computador**](c-computer.md)[**-**](c-domaindns.md)[**unidade organizacional**](c-organizationalunit.md) do DNS                   |
| Classes Auxiliares           | \-                                                                                                                                                                   |
| NT-Security-Descriptor      | O:BAG: INADEQUADO: S:                                                                                                                                                         |
| Descritor de segurança padrão | D: (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; PO) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; CO) (A;; RPLCLORC;;; AU |
| System-Flags                | 0x00000010                                                                                                                                                           |



## <a name="windows-server-2003-r2-attributes"></a>Windows Atributos do Server 2003 R2

essa classe contém os seguintes atributos para o Windows Server 2003 R2:



| Atributo                                                                   | Obrigatório | Derivado de                                                                             |
|-----------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------|
| [**Descrição do administrador**](a-admindescription.md)                             | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Administração – nome de exibição**](a-admindisplayname.md)                            | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Atributos permitidos**](a-allowedattributes.md)                           | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Permitido-atributos-efetivos**](a-allowedattributeseffective.md)        | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Classes filho permitidas**](a-allowedchildclasses.md)                      | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Permitido-filho-classes-efetivas**](a-allowedchildclasseseffective.md)   | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Número de ativos**](a-assetnumber.md)                                       | Falso     | **Fila de impressão**                                                                          |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)               | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Bytes por minuto**](a-bytesperminute.md)                                | Falso     | **Fila de impressão**                                                                          |
| [**Nome canônico**](a-canonicalname.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Nome comum**](a-cn.md)                                                 | Verdadeiro      | [**Ponto de conexão**](c-connectionpoint.md)<br/> [**Início**](c-top.md)<br/> |
| [**Criação-carimbo de data/hora**](a-createtimestamp.md)                              | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Prioridade padrão**](a-defaultpriority.md)                               | Falso     | **Fila de impressão**                                                                          |
| [**Descrição**](a-description.md)                                        | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Nome de exibição**](a-displayname.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Nome de exibição-imprimível**](a-displaynameprintable.md)                    | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Nome do driver**](a-drivername.md)                                         | Falso     | **Fila de impressão**                                                                          |
| [**Versão do driver**](a-driverversion.md)                                   | Falso     | **Fila de impressão**                                                                          |
| [**DSA-assinatura**](a-dsasignature.md)                                     | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**DS-Core-propagação-data**](a-dscorepropagationdata.md)                 | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Nome da extensão**](a-extensionname.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Flags**](a-flags.md)                                                    | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**De entrada**](a-fromentry.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                   | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                  | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Tipo de instância**](a-instancetype.md)                                     | Verdadeiro      | [**Início**](c-top.md)<br/>                                                          |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)               | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Is-Deleted**](a-isdeleted.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Is-Member-of-DL**](a-memberof.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                          | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Palavras-chave**](a-keywords.md)                                              | Falso     | [**Ponto de conexão**](c-connectionpoint.md)<br/>                                 |
| [**Último pai conhecido**](a-lastknownparent.md)                              | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Local**](a-location.md)                                              | Falso     | **Fila de Impressão**                                                                          |
| [**Gerenciado por**](a-managedby.md)                                           | Falso     | [**Ponto de conexão**](c-connectionpoint.md)<br/>                                 |
| [**Objetos gerenciados**](a-managedobjects.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Mastered-By**](a-masteredby.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Modificar carimbo de data/hora**](a-modifytimestamp.md)                              | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                 | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)         | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)             | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md) | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)      | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                              | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)           | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                       | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)    | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)  | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                         | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)               | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)     | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)     | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)      | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)              | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-Configurações**](a-msds-settings.md)                                   | Falso     | [**Ponto de conexão**](c-connectionpoint.md)<br/>                                 |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)               | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)               | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                  | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                    | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                     | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Descritor de segurança NT**](a-ntsecuritydescriptor.md)                    | Verdadeiro      | [**Início**](c-top.md)<br/>                                                          |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Categoria de objeto**](a-objectcategory.md)                                 | Verdadeiro      | [**Início**](c-top.md)<br/>                                                          |
| [**Classe de objeto**](a-objectclass.md)                                       | Verdadeiro      | [**Início**](c-top.md)<br/>                                                          |
| [**Guid de objeto**](a-objectguid.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Versão do objeto**](a-objectversion.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Sistema operacional**](a-operatingsystem.md)                               | Falso     | **Fila de Impressão**                                                                          |
| [**Hotfix do sistema operacional**](a-operatingsystemhotfix.md)                  | Falso     | **Fila de Impressão**                                                                          |
| [**Operating-System-Service-Pack**](a-operatingsystemservicepack.md)       | Falso     | **Fila de Impressão**                                                                          |
| [**Versão do sistema operacional**](a-operatingsystemversion.md)                | Falso     | **Fila de Impressão**                                                                          |
| [**Outros objetos conhecidos**](a-otherwellknownobjects.md)                 | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)   | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Conjunto de atributos parcial**](a-partialattributeset.md)                      | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Physical-Location-Object**](a-physicallocationobject.md)                | Falso     | **Fila de Impressão**                                                                          |
| [**Nome da porta**](a-portname.md)                                             | Falso     | **Fila de Impressão**                                                                          |
| [**Possíveis inferiores**](a-possibleinferiors.md)                           | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Atributos de impressão**](a-printattributes.md)                               | Falso     | **Fila de Impressão**                                                                          |
| [**Nomes de compartimento de impressão**](a-printbinnames.md)                                  | Falso     | **Fila de Impressão**                                                                          |
| [**Print-Collate**](a-printcollate.md)                                     | Falso     | **Fila de Impressão**                                                                          |
| [**Cor da impressão**](a-printcolor.md)                                         | Falso     | **Fila de Impressão**                                                                          |
| [**Com suporte para Print-Duplex**](a-printduplexsupported.md)                    | Falso     | **Fila de Impressão**                                                                          |
| [**Hora de término da impressão**](a-printendtime.md)                                    | Falso     | **Fila de Impressão**                                                                          |
| [**Nome da impressora**](a-printername.md)                                       | Verdadeiro      | **Fila de Impressão**                                                                          |
| [**Imprimir o nome do formulário**](a-printformname.md)                                  | Falso     | **Fila de Impressão**                                                                          |
| [**Print-Keep-Printed-Jobs**](a-printkeepprintedjobs.md)                   | Falso     | **Fila de Impressão**                                                                          |
| [**Linguagem de impressão**](a-printlanguage.md)                                   | Falso     | **Fila de Impressão**                                                                          |
| [**Imprimir-MAC-address**](a-printmacaddress.md)                              | Falso     | **Fila de impressão**                                                                          |
| [**Imprimir-Max-cópias**](a-printmaxcopies.md)                                | Falso     | **Fila de impressão**                                                                          |
| [**Impressão-Max-resolução-com suporte**](a-printmaxresolutionsupported.md)     | Falso     | **Fila de impressão**                                                                          |
| [**Impressão-Max-X-extensão**](a-printmaxxextent.md)                             | Falso     | **Fila de impressão**                                                                          |
| [**Impressão-Max-Y-extensão**](a-printmaxyextent.md)                             | Falso     | **Fila de impressão**                                                                          |
| [**Impressão-mídia pronta**](a-printmediaready.md)                              | Falso     | **Fila de impressão**                                                                          |
| [**Impressão-mídia-com suporte**](a-printmediasupported.md)                      | Falso     | **Fila de impressão**                                                                          |
| [**Memória de impressão**](a-printmemory.md)                                       | Falso     | **Fila de impressão**                                                                          |
| [**Impressão-min-X-extensão**](a-printminxextent.md)                             | Falso     | **Fila de impressão**                                                                          |
| [**Impressão-min-Y-extensão**](a-printminyextent.md)                             | Falso     | **Fila de impressão**                                                                          |
| [**Endereço de rede de impressão**](a-printnetworkaddress.md)                      | Falso     | **Fila de impressão**                                                                          |
| [**Imprimir-notificar**](a-printnotify.md)                                       | Falso     | **Fila de impressão**                                                                          |
| [**Imprimir-numeração**](a-printnumberup.md)                                  | Falso     | **Fila de impressão**                                                                          |
| [**Orientações de impressão-com suporte**](a-printorientationssupported.md)        | Falso     | **Fila de impressão**                                                                          |
| [**Imprimir-proprietário**](a-printowner.md)                                         | Falso     | **Fila de impressão**                                                                          |
| [**Imprimir páginas por minuto**](a-printpagesperminute.md)                     | Falso     | **Fila de impressão**                                                                          |
| [**Taxa de impressão**](a-printrate.md)                                           | Falso     | **Fila de impressão**                                                                          |
| [**Unidade de taxa de impressão**](a-printrateunit.md)                                  | Falso     | **Fila de impressão**                                                                          |
| [**Imprimir-separador de arquivo**](a-printseparatorfile.md)                        | Falso     | **Fila de impressão**                                                                          |
| [**Nome de compartilhamento de impressão**](a-printsharename.md)                                | Falso     | **Fila de impressão**                                                                          |
| [**Spool de impressão**](a-printspooling.md)                                   | Falso     | **Fila de impressão**                                                                          |
| [**Grampeamento de impressão-com suporte**](a-printstaplingsupported.md)                | Falso     | **Fila de impressão**                                                                          |
| [**Imprimir-hora de início**](a-printstarttime.md)                                | Falso     | **Fila de impressão**                                                                          |
| [**Status de impressão**](a-printstatus.md)                                       | Falso     | **Fila de impressão**                                                                          |
| [**Priority**](a-priority.md)                                              | Falso     | **Fila de impressão**                                                                          |
| [**Nome-do-objeto-proxy**](a-proxiedobjectname.md)                          | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Endereços de proxy**](a-proxyaddresses.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Consulta-política-BL**](a-querypolicybl.md)                                  | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**RDN**](a-name.md)                                                       | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Repl-Property-meta-data**](a-replpropertymetadata.md)                   | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Repl-UpToDate-vector**](a-repluptodatevector.md)                        | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Relatórios**](a-directreports.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Representantes-de**](a-repsfrom.md)                                             | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Reps-to**](a-repsto.md)                                                 | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Revisão**](a-revision.md)                                              | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                          | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Nome do servidor**](a-servername.md)                                         | Verdadeiro      | **Fila de Impressão**                                                                          |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Nome curto do servidor**](a-shortservername.md)                              | Verdadeiro      | **Fila de Impressão**                                                                          |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)              | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Classe Structural-Object**](a-structuralobjectclass.md)                  | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Sub-refs**](a-subrefs.md)                                               | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Sinalizadores de sistema**](a-systemflags.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Unc-Name**](a-uncname.md)                                               | Verdadeiro      | **Fila de Impressão**                                                                          |
| [**USN alterado**](a-usnchanged.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Criado por USN**](a-usncreated.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                  | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**UsN-Intersite**](a-usnintersite.md)                                     | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**USN-Source**](a-usnsource.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Número de versão**](a-versionnumber.md)                                   | Verdadeiro      | **Fila de Impressão**                                                                          |
| [**Wbem-Path**](a-wbempath.md)                                             | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Objetos conhecidos**](a-wellknownobjects.md)                            | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Quando alterado**](a-whenchanged.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Quando criado**](a-whencreated.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**WWW-Home Page**](a-wwwhomepage.md)                                      | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**WWW-Page-Other**](a-url.md)                                             | Falso     | [**Início**](c-top.md)<br/>                                                          |



## <a name="windows-server-2008"></a>Windows Server 2008

-   [Atributos](#windows-server-2008-attributes)



| Entrada | Valor |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                                                                                                |
| Object-Category             | 1                                                                                                                                                                    |
| Default-Object-Category     | \-                                                                                                                                                                   |
| Governs-Id                  | 1.2.840.113556.1.5.23                                                                                                                                                |
| Valor ocultado padrão        | 0                                                                                                                                                                    |
| Rdn-Att-Id                  | [**Common-Name**](a-cn.md)<br/>                                                                                                                               |
| Subclasse de                 | [**Ponto de conexão**](c-connectionpoint.md)<br/>                                                                                                             |
| Possíveis superiores          | [**Unidade**](c-computer.md)[**organizacional**](c-container.md)[**dns-de-domínio do contêiner**](c-domaindns.md)do [**computador**](c-organizationalunit.md)                   |
| Classes Auxiliares           | \-                                                                                                                                                                   |
| Descritor de segurança NT      | O:BAG:BAD:S:                                                                                                                                                         |
| Descritor de segurança padrão | D:(A;; RPWPCRCCDCLCLORCWOWDSDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDTSW;;; SY)(A;; RPWPCRCCDCLCLORCWOWDSDTSW;;; PO)(A;; RPWPCRCCDCLCLORCWOWDSDTSW;;; CO)(A;; RPLCLORC;;; AU) |
| System-Flags                | 0x00000010                                                                                                                                                           |



## <a name="windows-server-2008-attributes"></a>Windows Atributos do Server 2008

Essa classe contém os seguintes atributos para Windows Server 2008:



| Atributo                                                                      | Obrigatório | Derivado de                                                                             |
|--------------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------|
| [**Descrição do administrador**](a-admindescription.md)                                | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Admin-Display-Name**](a-admindisplayname.md)                               | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Atributos permitidos**](a-allowedattributes.md)                              | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)           | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Classes filho permitidas**](a-allowedchildclasses.md)                         | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)      | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Número do ativo**](a-assetnumber.md)                                          | Falso     | **Fila de Impressão**                                                                          |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                  | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Bytes por minuto**](a-bytesperminute.md)                                   | Falso     | **Fila de Impressão**                                                                          |
| [**Nome canônico**](a-canonicalname.md)                                      | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Common-Name**](a-cn.md)                                                    | Verdadeiro      | [**Ponto de conexão**](c-connectionpoint.md)<br/> [**Início**](c-top.md)<br/> |
| [**Criar carimbo de data/hora**](a-createtimestamp.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Prioridade padrão**](a-defaultpriority.md)                                  | Falso     | **Fila de Impressão**                                                                          |
| [**Descrição**](a-description.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Nome de exibição**](a-displayname.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Nome de exibição imprimível**](a-displaynameprintable.md)                       | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Nome do driver**](a-drivername.md)                                            | Falso     | **Fila de Impressão**                                                                          |
| [**Versão do driver**](a-driverversion.md)                                      | Falso     | **Fila de Impressão**                                                                          |
| [**Assinatura DSA**](a-dsasignature.md)                                        | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                    | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Nome da extensão**](a-extensionname.md)                                      | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Sinalizadores**](a-flags.md)                                                       | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Entrada de entrada**](a-fromentry.md)                                              | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                  | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                      | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                     | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Tipo de instância**](a-instancetype.md)                                        | Verdadeiro      | [**Início**](c-top.md)<br/>                                                          |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                  | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Is-Deleted**](a-isdeleted.md)                                              | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Is-Member-of-DL**](a-memberof.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                             | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Palavras-chave**](a-keywords.md)                                                 | Falso     | [**Ponto de conexão**](c-connectionpoint.md)<br/>                                 |
| [**Último-pai conhecido**](a-lastknownparent.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Local**](a-location.md)                                                 | Falso     | **Fila de impressão**                                                                          |
| [**Gerenciado por**](a-managedby.md)                                              | Falso     | [**Ponto de conexão**](c-connectionpoint.md)<br/>                                 |
| [**Objetos gerenciados**](a-managedobjects.md)                                    | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Mestre por**](a-masteredby.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Modificar-carimbo de data/hora**](a-modifytimestamp.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                    | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**MS-COM-userlink**](a-mscom-userlink.md)                                    | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)            | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-aprox-immed-subordinados**](a-msds-approx-immed-subordinates.md)    | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md) | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**MS-DS-Consistency-filho-Count**](a-ms-ds-consistencychildcount.md)         | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                      | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-is-domain-for**](a-msds-isdomainfor.md)                              | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-is-full-Replica-for**](a-msds-isfullreplicafor.md)                   | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-is-partial-Replica-for**](a-msds-ispartialreplicafor.md)             | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-KrbTgt-link-BL**](a-msds-krbtgtlinkbl.md)                            | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-Masterd-by**](a-msds-masteredby.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-Members-for-AZ-role-BL**](a-msds-membersforazrolebl.md)              | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-repl-cursores**](a-msds-ncreplcursors.md)                          | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-repl-Neighbors-Bounds**](a-msds-ncreplinboundneighbors.md)       | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-repl-Bound-Neighbors**](a-msds-ncreploutboundneighbors.md)     | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)  | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Tipo ms-DS-NC**](a-msds-nctype.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-non-members-BL**](a-msds-nonmembersbl.md)                            | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                  | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-Operations-for-AZ-role-BL**](a-msds-operationsforazrolebl.md)        | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)        | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-principal-Name**](a-msds-principalname.md)                           | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-PSO-aplicado**](a-msds-psoapplied.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-repl-Attribute-meta-data**](a-msds-replattributemetadata.md)         | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                 | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-Revealed-DSAs**](a-msds-revealeddsas.md)                             | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                        | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-Configurações**](a-msds-settings.md)                                      | Falso     | [**Ponto de conexão**](c-connectionpoint.md)<br/>                                 |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)                  | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                  | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                     | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                        | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Descritor de segurança NT**](a-ntsecuritydescriptor.md)                       | Verdadeiro      | [**Início**](c-top.md)<br/>                                                          |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Categoria de objeto**](a-objectcategory.md)                                    | Verdadeiro      | [**Início**](c-top.md)<br/>                                                          |
| [**Classe de objeto**](a-objectclass.md)                                          | Verdadeiro      | [**Início**](c-top.md)<br/>                                                          |
| [**Guid de objeto**](a-objectguid.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Versão do objeto**](a-objectversion.md)                                      | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Sistema operacional**](a-operatingsystem.md)                                  | Falso     | **Fila de Impressão**                                                                          |
| [**Hotfix do sistema operacional**](a-operatingsystemhotfix.md)                     | Falso     | **Fila de Impressão**                                                                          |
| [**Operating-System-Service-Pack**](a-operatingsystemservicepack.md)          | Falso     | **Fila de Impressão**                                                                          |
| [**Versão do sistema operacional**](a-operatingsystemversion.md)                   | Falso     | **Fila de Impressão**                                                                          |
| [**Outros objetos conhecidos**](a-otherwellknownobjects.md)                    | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)      | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Conjunto de atributos parcial**](a-partialattributeset.md)                         | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Physical-Location-Object**](a-physicallocationobject.md)                   | Falso     | **Fila de Impressão**                                                                          |
| [**Nome da porta**](a-portname.md)                                                | Falso     | **Fila de Impressão**                                                                          |
| [**Possíveis inferiores**](a-possibleinferiors.md)                              | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Atributos de impressão**](a-printattributes.md)                                  | Falso     | **Fila de Impressão**                                                                          |
| [**Nomes de compartimento de impressão**](a-printbinnames.md)                                     | Falso     | **Fila de Impressão**                                                                          |
| [**Print-Collate**](a-printcollate.md)                                        | Falso     | **Fila de Impressão**                                                                          |
| [**Cor da impressão**](a-printcolor.md)                                            | Falso     | **Fila de Impressão**                                                                          |
| [**Com suporte para Print-Duplex**](a-printduplexsupported.md)                       | Falso     | **Fila de Impressão**                                                                          |
| [**Hora de término da impressão**](a-printendtime.md)                                       | Falso     | **Fila de Impressão**                                                                          |
| [**Nome da impressora**](a-printername.md)                                          | Verdadeiro      | **Fila de Impressão**                                                                          |
| [**Imprimir o nome do formulário**](a-printformname.md)                                     | Falso     | **Fila de Impressão**                                                                          |
| [**Print-Keep-Printed-Jobs**](a-printkeepprintedjobs.md)                      | Falso     | **Fila de Impressão**                                                                          |
| [**Linguagem de impressão**](a-printlanguage.md)                                      | Falso     | **Fila de Impressão**                                                                          |
| [**Print-MAC-Address**](a-printmacaddress.md)                                 | Falso     | **Fila de Impressão**                                                                          |
| [**Print-Max-Copies**](a-printmaxcopies.md)                                   | Falso     | **Fila de Impressão**                                                                          |
| [**Print-Max-Resolution-Supported**](a-printmaxresolutionsupported.md)        | Falso     | **Fila de Impressão**                                                                          |
| [**Extensão Print-Max-X**](a-printmaxxextent.md)                                | Falso     | **Fila de Impressão**                                                                          |
| [**Extensão print-max-y**](a-printmaxyextent.md)                                | Falso     | **Fila de Impressão**                                                                          |
| [**Print-Media-Ready**](a-printmediaready.md)                                 | Falso     | **Fila de Impressão**                                                                          |
| [**Com suporte para mídia de impressão**](a-printmediasupported.md)                         | Falso     | **Fila de Impressão**                                                                          |
| [**Memória de impressão**](a-printmemory.md)                                          | Falso     | **Fila de Impressão**                                                                          |
| [**Extensão Print-Min-X**](a-printminxextent.md)                                | Falso     | **Fila de Impressão**                                                                          |
| [**Extensão print-min-y**](a-printminyextent.md)                                | Falso     | **Fila de Impressão**                                                                          |
| [**Print-Network-Address**](a-printnetworkaddress.md)                         | Falso     | **Fila de Impressão**                                                                          |
| [**Notificação de impressão**](a-printnotify.md)                                          | Falso     | **Fila de Impressão**                                                                          |
| [**Número de impressão**](a-printnumberup.md)                                     | Falso     | **Fila de Impressão**                                                                          |
| [**Orientação de impressão com suporte**](a-printorientationssupported.md)           | Falso     | **Fila de Impressão**                                                                          |
| [**Print-Owner**](a-printowner.md)                                            | Falso     | **Fila de Impressão**                                                                          |
| [**Imprimir páginas por minuto**](a-printpagesperminute.md)                        | Falso     | **Fila de Impressão**                                                                          |
| [**Taxa de impressão**](a-printrate.md)                                              | Falso     | **Fila de Impressão**                                                                          |
| [**Unidade de taxa de impressão**](a-printrateunit.md)                                     | Falso     | **Fila de Impressão**                                                                          |
| [**Print-Separator-File**](a-printseparatorfile.md)                           | Falso     | **Fila de Impressão**                                                                          |
| [**Print-Share-Name**](a-printsharename.md)                                   | Falso     | **Fila de Impressão**                                                                          |
| [**Spooling de impressão**](a-printspooling.md)                                      | Falso     | **Fila de Impressão**                                                                          |
| [**Com suporte para print-stapling**](a-printstaplingsupported.md)                   | Falso     | **Fila de Impressão**                                                                          |
| [**Print-Start-Time**](a-printstarttime.md)                                   | Falso     | **Fila de Impressão**                                                                          |
| [**Print-Status**](a-printstatus.md)                                          | Falso     | **Fila de Impressão**                                                                          |
| [**Priority**](a-priority.md)                                                 | Falso     | **Fila de Impressão**                                                                          |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                             | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Endereços proxy**](a-proxyaddresses.md)                                    | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Query-Policy-BL**](a-querypolicybl.md)                                     | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Rdn**](a-name.md)                                                          | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                      | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                           | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Relatórios**](a-directreports.md)                                             | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Representantes-de**](a-repsfrom.md)                                                | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Reps-to**](a-repsto.md)                                                    | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Revisão**](a-revision.md)                                                 | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**SD-direitos-efetivos**](a-sdrightseffective.md)                             | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Nome do servidor**](a-servername.md)                                            | Verdadeiro      | **Fila de impressão**                                                                          |
| [**Servidor-referência-BL**](a-serverreferencebl.md)                             | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Nome de servidor curto**](a-shortservername.md)                                 | Verdadeiro      | **Fila de impressão**                                                                          |
| [**Mostrar-in-avançado-somente exibição**](a-showinadvancedviewonly.md)                 | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Site-Object-BL**](a-siteobjectbl.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Classe de objeto estrutural**](a-structuralobjectclass.md)                     | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Sub-referências**](a-subrefs.md)                                                  | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                               | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Sinalizadores do sistema**](a-systemflags.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Nome UNC**](a-uncname.md)                                                  | Verdadeiro      | **Fila de impressão**                                                                          |
| [**USN-alterado**](a-usnchanged.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Criado pelo USN**](a-usncreated.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**USN-DSA-Last-obj-removido**](a-usndsalastobjremoved.md)                     | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**USN-entre sites**](a-usnintersite.md)                                        | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                    | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**USN-fonte**](a-usnsource.md)                                              | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Número de versão**](a-versionnumber.md)                                      | Verdadeiro      | **Fila de impressão**                                                                          |
| [**WBEM-caminho**](a-wbempath.md)                                                | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Objetos bem conhecidos**](a-wellknownobjects.md)                               | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Quando-alterado**](a-whenchanged.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Quando-criado**](a-whencreated.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**WWW-Home-Page**](a-wwwhomepage.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**WWW-página-outro**](a-url.md)                                                | Falso     | [**Início**](c-top.md)<br/>                                                          |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2

-   [Atributos](#windows-server-2008-r2-attributes)



| Entrada | Valor |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                                                                                                |
| Object-Category             | 1                                                                                                                                                                    |
| Categoria de objeto-padrão     | \-                                                                                                                                                                   |
| Governs-Id                  | 1.2.840.113556.1.5.23                                                                                                                                                |
| Padrão-ocultando valor        | 0                                                                                                                                                                    |
| RDN-ATT-ID                  | [**Nome comum**](a-cn.md)<br/>                                                                                                                               |
| Subclasse de                 | [**Ponto de conexão**](c-connectionpoint.md)<br/>                                                                                                             |
| Superiores possíveis          | Domínio do [**contêiner**](c-container.md)do [**computador**](c-computer.md)[**-**](c-domaindns.md)[**unidade organizacional**](c-organizationalunit.md) do DNS                   |
| Classes Auxiliares           | \-                                                                                                                                                                   |
| NT-Security-Descriptor      | O:BAG: INADEQUADO: S:                                                                                                                                                         |
| Descritor de segurança padrão | D: (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; PO) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; CO) (A;; RPLCLORC;;; AU |
| System-Flags                | 0x00000010                                                                                                                                                           |



## <a name="windows-server-2008-r2-attributes"></a>Windows Atributos do Server 2008 R2

essa classe contém os seguintes atributos para o Windows Server 2008 R2:



| Atributo                                                                        | Obrigatório | Derivado de                                                                             |
|----------------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------|
| [**Descrição do administrador**](a-admindescription.md)                                  | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Administração – nome de exibição**](a-admindisplayname.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Atributos permitidos**](a-allowedattributes.md)                                | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Permitido-atributos-efetivos**](a-allowedattributeseffective.md)             | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Classes filho permitidas**](a-allowedchildclasses.md)                           | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Permitido-filho-classes-efetivas**](a-allowedchildclasseseffective.md)        | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Número de ativos**](a-assetnumber.md)                                            | Falso     | **Fila de impressão**                                                                          |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                    | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Bytes por minuto**](a-bytesperminute.md)                                     | Falso     | **Fila de impressão**                                                                          |
| [**Nome canônico**](a-canonicalname.md)                                        | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Nome comum**](a-cn.md)                                                      | Verdadeiro      | [**Ponto de conexão**](c-connectionpoint.md)<br/> [**Início**](c-top.md)<br/> |
| [**Criação-carimbo de data/hora**](a-createtimestamp.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Prioridade padrão**](a-defaultpriority.md)                                    | Falso     | **Fila de impressão**                                                                          |
| [**Descrição**](a-description.md)                                             | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Nome de exibição**](a-displayname.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Nome de exibição-imprimível**](a-displaynameprintable.md)                         | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Nome do driver**](a-drivername.md)                                              | Falso     | **Fila de impressão**                                                                          |
| [**Versão do driver**](a-driverversion.md)                                        | Falso     | **Fila de impressão**                                                                          |
| [**DSA-assinatura**](a-dsasignature.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**DS-Core-propagação-data**](a-dscorepropagationdata.md)                      | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Nome da extensão**](a-extensionname.md)                                        | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Flags**](a-flags.md)                                                         | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**De entrada**](a-fromentry.md)                                                | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                    | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**FRS-member-Reference-BL**](a-frsmemberreferencebl.md)                        | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**FSMO-função-proprietário**](a-fsmoroleowner.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Tipo de instância**](a-instancetype.md)                                          | Verdadeiro      | [**Início**](c-top.md)<br/>                                                          |
| [**É-crítico-System-Object**](a-iscriticalsystemobject.md)                    | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Is-Deleted**](a-isdeleted.md)                                                | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Is-Member-of-DL**](a-memberof.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                               | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Is-Recycled**](a-isrecycled.md)                                              | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Palavras-chave**](a-keywords.md)                                                   | Falso     | [**Ponto de conexão**](c-connectionpoint.md)<br/>                                 |
| [**Último pai conhecido**](a-lastknownparent.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Local**](a-location.md)                                                   | Falso     | **Fila de Impressão**                                                                          |
| [**Gerenciado por**](a-managedby.md)                                                | Falso     | [**Ponto de conexão**](c-connectionpoint.md)<br/>                                 |
| [**Objetos gerenciados**](a-managedobjects.md)                                      | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Mastered-By**](a-masteredby.md)                                              | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Modificar carimbo de data/hora**](a-modifytimestamp.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                      | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                      | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)              | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                  | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)      | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)   | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)           | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                        | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-Enabled-Feature-BL**](a-msds-enabledfeaturebl.md)                      | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)             | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-Is-Domain-For**](a-msds-isdomainfor.md)                                | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-Is-Full-Replica-for**](a-msds-isfullreplicafor.md)                     | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-Is-Partial-Replica-for**](a-msds-ispartialreplicafor.md)               | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                              | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                              | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-local-Effective-Deletion-Time**](a-msds-localeffectivedeletiontime.md) | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-local-Effective-Recycle-Time**](a-msds-localeffectiverecycletime.md)   | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)                | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                            | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)         | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)       | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)    | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Tipo ms-DS-NC**](a-msds-nctype.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                              | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                    | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-OIDToGroup-Link-BL**](a-msds-oidtogrouplinkbl.md)                      | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)          | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)          | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                             | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-PSO-Applied**](a-msds-psoapplied.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)           | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                   | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-Revealed-DSAs**](a-msds-revealeddsas.md)                               | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                          | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-Configurações**](a-msds-settings.md)                                        | Falso     | [**Ponto de conexão**](c-connectionpoint.md)<br/>                                 |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)                    | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                    | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                       | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                          | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Descritor de segurança NT**](a-ntsecuritydescriptor.md)                         | Verdadeiro      | [**Início**](c-top.md)<br/>                                                          |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                     | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Categoria de objeto**](a-objectcategory.md)                                      | Verdadeiro      | [**Início**](c-top.md)<br/>                                                          |
| [**Classe de objeto**](a-objectclass.md)                                            | Verdadeiro      | [**Início**](c-top.md)<br/>                                                          |
| [**Guid de objeto**](a-objectguid.md)                                              | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Versão do objeto**](a-objectversion.md)                                        | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Sistema operacional**](a-operatingsystem.md)                                    | Falso     | **Fila de Impressão**                                                                          |
| [**Hotfix do sistema operacional**](a-operatingsystemhotfix.md)                       | Falso     | **Fila de Impressão**                                                                          |
| [**Operating-System-Service-Pack**](a-operatingsystemservicepack.md)            | Falso     | **Fila de Impressão**                                                                          |
| [**Versão do sistema operacional**](a-operatingsystemversion.md)                     | Falso     | **Fila de Impressão**                                                                          |
| [**Outros objetos conhecidos**](a-otherwellknownobjects.md)                      | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)        | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Conjunto de atributos parcial**](a-partialattributeset.md)                           | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Physical-Location-Object**](a-physicallocationobject.md)                     | Falso     | **Fila de Impressão**                                                                          |
| [**Nome da porta**](a-portname.md)                                                  | Falso     | **Fila de Impressão**                                                                          |
| [**Possíveis inferiores**](a-possibleinferiors.md)                                | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Atributos de impressão**](a-printattributes.md)                                    | Falso     | **Fila de Impressão**                                                                          |
| [**Nomes de compartimento de impressão**](a-printbinnames.md)                                       | Falso     | **Fila de Impressão**                                                                          |
| [**Print-Collate**](a-printcollate.md)                                          | Falso     | **Fila de Impressão**                                                                          |
| [**Cor da impressão**](a-printcolor.md)                                              | Falso     | **Fila de Impressão**                                                                          |
| [**Com suporte para Print-Duplex**](a-printduplexsupported.md)                         | Falso     | **Fila de Impressão**                                                                          |
| [**Hora de término da impressão**](a-printendtime.md)                                         | Falso     | **Fila de Impressão**                                                                          |
| [**Nome da impressora**](a-printername.md)                                            | Verdadeiro      | **Fila de Impressão**                                                                          |
| [**Imprimir o nome do formulário**](a-printformname.md)                                       | Falso     | **Fila de Impressão**                                                                          |
| [**Print-Keep-Printed-Jobs**](a-printkeepprintedjobs.md)                        | Falso     | **Fila de Impressão**                                                                          |
| [**Linguagem de impressão**](a-printlanguage.md)                                        | Falso     | **Fila de Impressão**                                                                          |
| [**Print-MAC-Address**](a-printmacaddress.md)                                   | Falso     | **Fila de Impressão**                                                                          |
| [**Print-Max-Copies**](a-printmaxcopies.md)                                     | Falso     | **Fila de Impressão**                                                                          |
| [**Print-Max-Resolution-Supported**](a-printmaxresolutionsupported.md)          | Falso     | **Fila de Impressão**                                                                          |
| [**Extensão Print-Max-X**](a-printmaxxextent.md)                                  | Falso     | **Fila de Impressão**                                                                          |
| [**Extensão print-max-y**](a-printmaxyextent.md)                                  | Falso     | **Fila de Impressão**                                                                          |
| [**Print-Media-Ready**](a-printmediaready.md)                                   | Falso     | **Fila de Impressão**                                                                          |
| [**Com suporte para mídia de impressão**](a-printmediasupported.md)                           | Falso     | **Fila de Impressão**                                                                          |
| [**Memória de impressão**](a-printmemory.md)                                            | Falso     | **Fila de Impressão**                                                                          |
| [**Extensão Print-Min-X**](a-printminxextent.md)                                  | Falso     | **Fila de Impressão**                                                                          |
| [**Extensão print-min-y**](a-printminyextent.md)                                  | Falso     | **Fila de Impressão**                                                                          |
| [**Print-Network-Address**](a-printnetworkaddress.md)                           | Falso     | **Fila de Impressão**                                                                          |
| [**Notificação de impressão**](a-printnotify.md)                                            | Falso     | **Fila de Impressão**                                                                          |
| [**Número de impressão**](a-printnumberup.md)                                       | Falso     | **Fila de Impressão**                                                                          |
| [**Orientação de impressão com suporte**](a-printorientationssupported.md)             | Falso     | **Fila de Impressão**                                                                          |
| [**Print-Owner**](a-printowner.md)                                              | Falso     | **Fila de Impressão**                                                                          |
| [**Imprimir páginas por minuto**](a-printpagesperminute.md)                          | Falso     | **Fila de Impressão**                                                                          |
| [**Taxa de impressão**](a-printrate.md)                                                | Falso     | **Fila de Impressão**                                                                          |
| [**Unidade de taxa de impressão**](a-printrateunit.md)                                       | Falso     | **Fila de Impressão**                                                                          |
| [**Print-Separator-File**](a-printseparatorfile.md)                             | Falso     | **Fila de Impressão**                                                                          |
| [**Print-Share-Name**](a-printsharename.md)                                     | Falso     | **Fila de Impressão**                                                                          |
| [**Spooling de impressão**](a-printspooling.md)                                        | Falso     | **Fila de Impressão**                                                                          |
| [**Com suporte para print-stapling**](a-printstaplingsupported.md)                     | Falso     | **Fila de Impressão**                                                                          |
| [**Print-Start-Time**](a-printstarttime.md)                                     | Falso     | **Fila de Impressão**                                                                          |
| [**Print-Status**](a-printstatus.md)                                            | Falso     | **Fila de Impressão**                                                                          |
| [**Priority**](a-priority.md)                                                   | Falso     | **Fila de Impressão**                                                                          |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                               | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Endereços proxy**](a-proxyaddresses.md)                                      | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Query-Policy-BL**](a-querypolicybl.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Rdn**](a-name.md)                                                            | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                        | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                             | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Relatórios**](a-directreports.md)                                               | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Reps-From**](a-repsfrom.md)                                                  | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Reps-To**](a-repsto.md)                                                      | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Revisão**](a-revision.md)                                                   | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                               | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Nome do servidor**](a-servername.md)                                              | Verdadeiro      | **Fila de Impressão**                                                                          |
| [**Server-Reference-BL**](a-serverreferencebl.md)                               | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Nome curto do servidor**](a-shortservername.md)                                   | Verdadeiro      | **Fila de Impressão**                                                                          |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)                   | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Site-Object-BL**](a-siteobjectbl.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Classe Structural-Object**](a-structuralobjectclass.md)                       | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Sub-refs**](a-subrefs.md)                                                    | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Sinalizadores de sistema**](a-systemflags.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Unc-Name**](a-uncname.md)                                                    | Verdadeiro      | **Fila de Impressão**                                                                          |
| [**USN alterado**](a-usnchanged.md)                                              | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Criado por USN**](a-usncreated.md)                                              | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                       | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**UsN-Intersite**](a-usnintersite.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                      | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**USN-Source**](a-usnsource.md)                                                | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Número de versão**](a-versionnumber.md)                                        | Verdadeiro      | **Fila de Impressão**                                                                          |
| [**Wbem-Path**](a-wbempath.md)                                                  | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Objetos bem conhecidos**](a-wellknownobjects.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Quando-alterado**](a-whenchanged.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Quando-criado**](a-whencreated.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**WWW-Home-Page**](a-wwwhomepage.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**WWW-página-outro**](a-url.md)                                                  | Falso     | [**Início**](c-top.md)<br/>                                                          |



## <a name="windows-server-2012"></a>Windows Server 2012

-   [Atributos](#windows-server-2012-attributes)



| Entrada | Valor |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                                                                                                |
| Object-Category             | 1                                                                                                                                                                    |
| Categoria de objeto-padrão     | \-                                                                                                                                                                   |
| Governs-Id                  | 1.2.840.113556.1.5.23                                                                                                                                                |
| Padrão-ocultando valor        | 0                                                                                                                                                                    |
| RDN-ATT-ID                  | [**Nome comum**](a-cn.md)<br/>                                                                                                                               |
| Subclasse de                 | [**Ponto de conexão**](c-connectionpoint.md)<br/>                                                                                                             |
| Superiores possíveis          | Domínio do [**contêiner**](c-container.md)do [**computador**](c-computer.md)[**-**](c-domaindns.md)[**unidade organizacional**](c-organizationalunit.md) do DNS                   |
| Classes Auxiliares           | \-                                                                                                                                                                   |
| NT-Security-Descriptor      | O:BAG: INADEQUADO: S:                                                                                                                                                         |
| Descritor de segurança padrão | D: (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; PO) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; CO) (A;; RPLCLORC;;; AU |
| System-Flags                | 0x00000010                                                                                                                                                           |



## <a name="windows-server-2012-attributes"></a>Windows Server 2012 Atributos

Essa classe contém os seguintes atributos para Windows Server 2012:



| Atributo                                                                                    | Obrigatório | Derivado de                                                                             |
|----------------------------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------|
| [**Descrição do administrador**](a-admindescription.md)                                              | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Administração – nome de exibição**](a-admindisplayname.md)                                             | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Atributos permitidos**](a-allowedattributes.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Permitido-atributos-efetivos**](a-allowedattributeseffective.md)                         | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Classes filho permitidas**](a-allowedchildclasses.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Permitido-filho-classes-efetivas**](a-allowedchildclasseseffective.md)                    | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Número de ativos**](a-assetnumber.md)                                                        | Falso     | **Fila de impressão**                                                                          |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                                | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Bytes por minuto**](a-bytesperminute.md)                                                 | Falso     | **Fila de impressão**                                                                          |
| [**Nome canônico**](a-canonicalname.md)                                                    | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Nome comum**](a-cn.md)                                                                  | Verdadeiro      | [**Ponto de conexão**](c-connectionpoint.md)<br/> [**Início**](c-top.md)<br/> |
| [**Criação-carimbo de data/hora**](a-createtimestamp.md)                                               | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Prioridade padrão**](a-defaultpriority.md)                                                | Falso     | **Fila de impressão**                                                                          |
| [**Descrição**](a-description.md)                                                         | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Nome de exibição**](a-displayname.md)                                                        | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Nome de exibição-imprimível**](a-displaynameprintable.md)                                     | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Nome do driver**](a-drivername.md)                                                          | Falso     | **Fila de impressão**                                                                          |
| [**Versão do driver**](a-driverversion.md)                                                    | Falso     | **Fila de Impressão**                                                                          |
| [**Assinatura DSA**](a-dsasignature.md)                                                      | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                                  | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Nome da extensão**](a-extensionname.md)                                                    | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Sinalizadores**](a-flags.md)                                                                     | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Entrada de entrada**](a-fromentry.md)                                                            | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                                | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                                    | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                                   | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Tipo de instância**](a-instancetype.md)                                                      | Verdadeiro      | [**Início**](c-top.md)<br/>                                                          |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                                | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Is-Deleted**](a-isdeleted.md)                                                            | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Is-Member-of-DL**](a-memberof.md)                                                        | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Is-Recycled**](a-isrecycled.md)                                                          | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Palavras-chave**](a-keywords.md)                                                               | Falso     | [**Ponto de conexão**](c-connectionpoint.md)<br/>                                 |
| [**Último pai conhecido**](a-lastknownparent.md)                                               | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Local**](a-location.md)                                                               | Falso     | **Fila de Impressão**                                                                          |
| [**Gerenciado por**](a-managedby.md)                                                            | Falso     | [**Ponto de conexão**](c-connectionpoint.md)<br/>                                 |
| [**Objetos gerenciados**](a-managedobjects.md)                                                  | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Mastered-By**](a-masteredby.md)                                                          | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Modificar carimbo de data/hora**](a-modifytimestamp.md)                                               | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                                  | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                                  | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)                          | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                              | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)                  | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)               | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-Claim-Shares-Possible-Values-With-BL**](a-msds-claimsharespossiblevalueswithbl.md) | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)                       | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                                    | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-Enabled-Feature-BL**](a-msds-enabledfeaturebl.md)                                  | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)                         | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-Is-Domain-For**](a-msds-isdomainfor.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-Is-Full-Replica-for**](a-msds-isfullreplicafor.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-Is-Partial-Replica-for**](a-msds-ispartialreplicafor.md)                           | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-Is-Primary-Computer-For**](a-msds-isprimarycomputerfor.md)                         | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-local-Effective-Deletion-Time**](a-msds-localeffectivedeletiontime.md)             | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-local-Effective-Recycle-Time**](a-msds-localeffectiverecycletime.md)               | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                                               | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)                            | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-Members-Of-Resource-Property-List-BL**](a-msds-membersofresourcepropertylistbl.md) | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                                        | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)                     | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)                   | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)                | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Tipo ms-DS-NC**](a-msds-nctype.md)                                                       | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                                | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-OIDToGroup-Link-BL**](a-msds-oidtogrouplinkbl.md)                                  | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)                      | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)                      | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-PSO-Applied**](a-msds-psoapplied.md)                                               | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)                       | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                               | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-Revealed-DSAs**](a-msds-revealeddsas.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                                      | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-Configurações**](a-msds-settings.md)                                                    | Falso     | [**Ponto de conexão**](c-connectionpoint.md)<br/>                                 |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)                                | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                                | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-TDO-Egress-BL**](a-msds-tdoegressbl.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-TDO-Ingress-BL**](a-msds-tdoingressbl.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-DS-Value-Type-Reference-BL**](a-msds-valuetypereferencebl.md)                         | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                                        | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**msSFU-30-POSIX-membro de**](a-mssfu30posixmemberof.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                                     | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Não Security-Member-BL**](a-nonsecuritymemberbl.md)                                      | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                                     | Verdadeiro      | [**Início**](c-top.md)<br/>                                                          |
| [**Obj-dist-Name**](a-distinguishedname.md)                                                 | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Objeto-categoria**](a-objectcategory.md)                                                  | Verdadeiro      | [**Início**](c-top.md)<br/>                                                          |
| [**Classe de objeto**](a-objectclass.md)                                                        | Verdadeiro      | [**Início**](c-top.md)<br/>                                                          |
| [**GUID do objeto**](a-objectguid.md)                                                          | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Versão do objeto**](a-objectversion.md)                                                    | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Sistema operacional**](a-operatingsystem.md)                                                | Falso     | **Fila de impressão**                                                                          |
| [**Operating-System-hotfix**](a-operatingsystemhotfix.md)                                   | Falso     | **Fila de impressão**                                                                          |
| [**Sistema operacional-Service-Pack**](a-operatingsystemservicepack.md)                        | Falso     | **Fila de impressão**                                                                          |
| [**Versão do sistema operacional**](a-operatingsystemversion.md)                                 | Falso     | **Fila de impressão**                                                                          |
| [**Outros objetos bem conhecidos**](a-otherwellknownobjects.md)                                  | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Parcial-atributo-exclusão-lista**](a-partialattributedeletionlist.md)                    | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Conjunto de atributos parciais**](a-partialattributeset.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Físico-local-objeto**](a-physicallocationobject.md)                                 | Falso     | **Fila de impressão**                                                                          |
| [**Nome da porta**](a-portname.md)                                                              | Falso     | **Fila de impressão**                                                                          |
| [**Possíveis-inferiores**](a-possibleinferiors.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Imprimir atributos**](a-printattributes.md)                                                | Falso     | **Fila de impressão**                                                                          |
| [**Print-bin-Names**](a-printbinnames.md)                                                   | Falso     | **Fila de impressão**                                                                          |
| [**Imprimir-agrupar**](a-printcollate.md)                                                      | Falso     | **Fila de impressão**                                                                          |
| [**Cor de impressão**](a-printcolor.md)                                                          | Falso     | **Fila de impressão**                                                                          |
| [**Impressão-duplex-com suporte**](a-printduplexsupported.md)                                     | Falso     | **Fila de impressão**                                                                          |
| [**Impressão – hora de término**](a-printendtime.md)                                                     | Falso     | **Fila de impressão**                                                                          |
| [**Nome da impressora**](a-printername.md)                                                        | Verdadeiro      | **Fila de impressão**                                                                          |
| [**Nome do formulário de impressão**](a-printformname.md)                                                   | Falso     | **Fila de impressão**                                                                          |
| [**Imprimir-manter-impresso-trabalhos**](a-printkeepprintedjobs.md)                                    | Falso     | **Fila de impressão**                                                                          |
| [**Idioma de impressão**](a-printlanguage.md)                                                    | Falso     | **Fila de impressão**                                                                          |
| [**Imprimir-MAC-address**](a-printmacaddress.md)                                               | Falso     | **Fila de impressão**                                                                          |
| [**Imprimir-Max-cópias**](a-printmaxcopies.md)                                                 | Falso     | **Fila de impressão**                                                                          |
| [**Impressão-Max-resolução-com suporte**](a-printmaxresolutionsupported.md)                      | Falso     | **Fila de impressão**                                                                          |
| [**Impressão-Max-X-extensão**](a-printmaxxextent.md)                                              | Falso     | **Fila de impressão**                                                                          |
| [**Impressão-Max-Y-extensão**](a-printmaxyextent.md)                                              | Falso     | **Fila de impressão**                                                                          |
| [**Impressão-mídia pronta**](a-printmediaready.md)                                               | Falso     | **Fila de impressão**                                                                          |
| [**Impressão-mídia-com suporte**](a-printmediasupported.md)                                       | Falso     | **Fila de impressão**                                                                          |
| [**Memória de impressão**](a-printmemory.md)                                                        | Falso     | **Fila de impressão**                                                                          |
| [**Impressão-min-X-extensão**](a-printminxextent.md)                                              | Falso     | **Fila de impressão**                                                                          |
| [**Impressão-min-Y-extensão**](a-printminyextent.md)                                              | Falso     | **Fila de impressão**                                                                          |
| [**Endereço de rede de impressão**](a-printnetworkaddress.md)                                       | Falso     | **Fila de impressão**                                                                          |
| [**Imprimir-notificar**](a-printnotify.md)                                                        | Falso     | **Fila de impressão**                                                                          |
| [**Imprimir-numeração**](a-printnumberup.md)                                                   | Falso     | **Fila de impressão**                                                                          |
| [**Orientações de impressão-com suporte**](a-printorientationssupported.md)                         | Falso     | **Fila de impressão**                                                                          |
| [**Imprimir-proprietário**](a-printowner.md)                                                          | Falso     | **Fila de impressão**                                                                          |
| [**Imprimir páginas por minuto**](a-printpagesperminute.md)                                      | Falso     | **Fila de impressão**                                                                          |
| [**Taxa de impressão**](a-printrate.md)                                                            | Falso     | **Fila de impressão**                                                                          |
| [**Unidade de taxa de impressão**](a-printrateunit.md)                                                   | Falso     | **Fila de impressão**                                                                          |
| [**Imprimir-separador de arquivo**](a-printseparatorfile.md)                                         | Falso     | **Fila de impressão**                                                                          |
| [**Nome de compartilhamento de impressão**](a-printsharename.md)                                                 | Falso     | **Fila de impressão**                                                                          |
| [**Spool de impressão**](a-printspooling.md)                                                    | Falso     | **Fila de impressão**                                                                          |
| [**Grampeamento de impressão-com suporte**](a-printstaplingsupported.md)                                 | Falso     | **Fila de impressão**                                                                          |
| [**Imprimir-hora de início**](a-printstarttime.md)                                                 | Falso     | **Fila de impressão**                                                                          |
| [**Status de impressão**](a-printstatus.md)                                                        | Falso     | **Fila de impressão**                                                                          |
| [**Priority**](a-priority.md)                                                               | Falso     | **Fila de impressão**                                                                          |
| [**Nome-do-objeto-proxy**](a-proxiedobjectname.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Endereços de proxy**](a-proxyaddresses.md)                                                  | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Consulta-política-BL**](a-querypolicybl.md)                                                   | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**RDN**](a-name.md)                                                                        | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Repl-Property-meta-data**](a-replpropertymetadata.md)                                    | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Repl-UpToDate-vector**](a-repluptodatevector.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Relatórios**](a-directreports.md)                                                           | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Representantes-de**](a-repsfrom.md)                                                              | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Reps-to**](a-repsto.md)                                                                  | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Revisão**](a-revision.md)                                                               | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**SD-direitos-efetivos**](a-sdrightseffective.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Nome do servidor**](a-servername.md)                                                          | Verdadeiro      | **Fila de impressão**                                                                          |
| [**Servidor-referência-BL**](a-serverreferencebl.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Nome de servidor curto**](a-shortservername.md)                                               | Verdadeiro      | **Fila de impressão**                                                                          |
| [**Mostrar-in-avançado-somente exibição**](a-showinadvancedviewonly.md)                               | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Site-Object-BL**](a-siteobjectbl.md)                                                     | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Classe de objeto estrutural**](a-structuralobjectclass.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Sub-referências**](a-subrefs.md)                                                                | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                             | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Sinalizadores do sistema**](a-systemflags.md)                                                        | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Nome UNC**](a-uncname.md)                                                                | Verdadeiro      | **Fila de impressão**                                                                          |
| [**USN-alterado**](a-usnchanged.md)                                                          | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Criado pelo USN**](a-usncreated.md)                                                          | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**USN-DSA-Last-obj-removido**](a-usndsalastobjremoved.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**USN-entre sites**](a-usnintersite.md)                                                      | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                                  | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**USN-fonte**](a-usnsource.md)                                                            | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Número de versão**](a-versionnumber.md)                                                    | Verdadeiro      | **Fila de impressão**                                                                          |
| [**WBEM-caminho**](a-wbempath.md)                                                              | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Objetos bem conhecidos**](a-wellknownobjects.md)                                             | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Quando-alterado**](a-whenchanged.md)                                                        | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**Quando-criado**](a-whencreated.md)                                                        | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**WWW-Home-Page**](a-wwwhomepage.md)                                                       | Falso     | [**Início**](c-top.md)<br/>                                                          |
| [**WWW-página-outro**](a-url.md)                                                              | Falso     | [**Início**](c-top.md)<br/>                                                          |



 

 





