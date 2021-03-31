---
title: Classe NTDS-DSA
description: Representa o Active Directory processo DSA no servidor.
ms.assetid: f4369122-d74a-45d2-9dc0-46894a9f99cc
ms.tgt_platform: multiple
keywords:
- Esquema de AD da classe NTDS-DSA
- Esquema de AD da classe nTDSDSA
topic_type:
- apiref
api_name:
- NTDS-DSA
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f64606c07aa15aaf7d75e7bbcdb1caf06ed84ac
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103645390"
---
# <a name="ntds-dsa-class"></a>Classe NTDS-DSA

Representa o Active Directory processo DSA no servidor.



| Entrada | Valor |
|-------------------|--------------------------------------|
| CN                | NTDS-DSA                             |
| LDAP-Display-Name | nTDSDSA                              |
| Privilégio de atualização  | \-                                   |
| Frequência de atualização  | \-                                   |
| Schema-ID-GUID    | f0f8ffab-1191-11d0-a060-00aa006c33ed |



## <a name="implementations"></a>Implementações

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**ADAM**](#adam-attributes)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server

-   [Atributos](#windows-2000-server-attributes)
-   [Direitos estendidos](#windows-2000-server-extended-rights)



| Entrada | Valor |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | True                                                                                         |
| Object-Category             | 1                                                                                            |
| Categoria de objeto-padrão     | \-                                                                                           |
| Governs-Id                  | 1.2.840.113556.1.5.7000.47                                                                   |
| Padrão-ocultando valor        | 1                                                                                            |
| RDN-ATT-ID                  | [**Nome comum**](a-cn.md)<br/>                                                       |
| Subclasse de                 | [**Aplicativo-configurações**](c-applicationsettings.md)<br/>                             |
| Superiores possíveis          | [**Organização do servidor**](c-server.md)[](c-organization.md)                             |
| Classes Auxiliares           | \-                                                                                           |
| NT-Security-Descriptor      | O:BAG: INADEQUADO: S:                                                                                 |
| Descritor de segurança padrão | D: (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A;; RPLCLORC;;; AU |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-2000-server-attributes"></a>Atributos do Windows 2000 Server

Essa classe contém os seguintes atributos para o Windows 2000 Server:



| Atributo                                                                 | Obrigatório | Derivado de                                                     |
|---------------------------------------------------------------------------|-----------|------------------------------------------------------------------|
| [**Descrição do administrador**](a-admindescription.md)                           | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Administração – nome de exibição**](a-admindisplayname.md)                          | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Atributos permitidos**](a-allowedattributes.md)                         | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Permitido-atributos-efetivos**](a-allowedattributeseffective.md)      | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Classes filho permitidas**](a-allowedchildclasses.md)                    | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Permitido-filho-classes-efetivas**](a-allowedchildclasseseffective.md) | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Nome do aplicativo**](a-applicationname.md)                             | Falso     | [**Aplicativo-configurações**](c-applicationsettings.md)<br/> |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)             | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Nome canônico**](a-canonicalname.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Nome comum**](a-cn.md)                                               | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Criação-carimbo de data/hora**](a-createtimestamp.md)                            | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Descrição**](a-description.md)                                      | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Nome de exibição**](a-displayname.md)                                     | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Nome de exibição-imprimível**](a-displaynameprintable.md)                  | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**DMD-local**](a-dmdlocation.md)                                     | Falso     | **NTDS-DSA**                                                     |
| [**DSA-assinatura**](a-dsasignature.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**DS-Core-propagação-data**](a-dscorepropagationdata.md)               | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Nome da extensão**](a-extensionname.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Flags**](a-flags.md)                                                  | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**De entrada**](a-fromentry.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)             | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**FRS-member-Reference-BL**](a-frsmemberreferencebl.md)                 | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**FRS-raiz-caminho**](a-frsrootpath.md)                                    | Falso     | **NTDS-DSA**                                                     |
| [**FSMO-função-proprietário**](a-fsmoroleowner.md)                                | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Tem-mestre-NCs**](a-hasmasterncs.md)                                  | Falso     | **NTDS-DSA**                                                     |
| [**De-parcial-réplica-NCs**](a-haspartialreplicancs.md)                 | Falso     | **NTDS-DSA**                                                     |
| [**Tipo de instância**](a-instancetype.md)                                   | True      | [**Início**](c-top.md)<br/>                                  |
| [**ID de invocação**](a-invocationid.md)                                   | Falso     | **NTDS-DSA**                                                     |
| [**É-crítico-System-Object**](a-iscriticalsystemobject.md)             | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**É excluído**](a-isdeleted.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Is-member-of-DL**](a-memberof.md)                                     | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**É com proprietário de privilégio**](a-isprivilegeholder.md)                        | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Último backup-tempo de restauração**](a-lastbackuprestorationtime.md)       | Falso     | **NTDS-DSA**                                                     |
| [**Último-pai conhecido**](a-lastknownparent.md)                            | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Gerenciado por**](a-managedby.md)                                         | Falso     | **NTDS-DSA**                                                     |
| [**Objetos gerenciados**](a-managedobjects.md)                               | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Mestre por**](a-masteredby.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Modificar-carimbo de data/hora**](a-modifytimestamp.md)                            | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**MS-DS-Consistency-filho-Count**](a-ms-ds-consistencychildcount.md)    | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                 | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                  | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Endereço de rede**](a-networkaddress.md)                               | Falso     | **NTDS-DSA**                                                     |
| [**Não Security-Member-BL**](a-nonsecuritymemberbl.md)                   | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Lista de notificações**](a-notificationlist.md)                           | Falso     | [**Aplicativo-configurações**](c-applicationsettings.md)<br/> |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                  | True      | [**Início**](c-top.md)<br/>                                  |
| [**Obj-dist-Name**](a-distinguishedname.md)                              | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Objeto-categoria**](a-objectcategory.md)                               | True      | [**Início**](c-top.md)<br/>                                  |
| [**Classe de objeto**](a-objectclass.md)                                     | True      | [**Início**](c-top.md)<br/>                                  |
| [**GUID do objeto**](a-objectguid.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Versão do objeto**](a-objectversion.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Opções**](a-options.md)                                              | Falso     | **NTDS-DSA**                                                     |
| [**Outros objetos bem conhecidos**](a-otherwellknownobjects.md)               | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Parcial-atributo-exclusão-lista**](a-partialattributedeletionlist.md) | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Conjunto de atributos parciais**](a-partialattributeset.md)                    | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Possíveis-inferiores**](a-possibleinferiors.md)                         | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Nome-do-objeto-proxy**](a-proxiedobjectname.md)                        | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Endereços de proxy**](a-proxyaddresses.md)                               | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Consulta-política-BL**](a-querypolicybl.md)                                | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Consulta-política-objeto**](a-querypolicyobject.md)                        | Falso     | **NTDS-DSA**                                                     |
| [**RDN**](a-name.md)                                                     | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Repl-Property-meta-data**](a-replpropertymetadata.md)                 | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Repl-UpToDate-vector**](a-repluptodatevector.md)                      | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Relatórios**](a-directreports.md)                                        | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Representantes-de**](a-repsfrom.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Reps-to**](a-repsto.md)                                               | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Desativado-repl-DSA-Signatures**](a-retiredrepldsasignatures.md)         | Falso     | **NTDS-DSA**                                                     |
| [**Revisão**](a-revision.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**SD-direitos-efetivos**](a-sdrightseffective.md)                        | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Referência de servidor**](a-serverreference.md)                             | Falso     | **NTDS-DSA**                                                     |
| [**Servidor-referência-BL**](a-serverreferencebl.md)                        | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Mostrar-in-avançado-somente exibição**](a-showinadvancedviewonly.md)            | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Site-Object-BL**](a-siteobjectbl.md)                                  | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Sub-referências**](a-subrefs.md)                                             | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                          | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Sinalizadores do sistema**](a-systemflags.md)                                     | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**USN-alterado**](a-usnchanged.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Criado pelo USN**](a-usncreated.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**USN-DSA-Last-obj-removido**](a-usndsalastobjremoved.md)                | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**USN-entre sites**](a-usnintersite.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                               | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**USN-fonte**](a-usnsource.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**WBEM-caminho**](a-wbempath.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Objetos bem conhecidos**](a-wellknownobjects.md)                          | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Quando-alterado**](a-whenchanged.md)                                     | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Quando-criado**](a-whencreated.md)                                     | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**WWW-Home-Page**](a-wwwhomepage.md)                                    | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**WWW-página-outro**](a-url.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                  |



## <a name="windows-2000-server-extended-rights"></a>Direitos estendidos do Windows 2000 Server

Essa classe contém os seguintes direitos estendidos para o Windows 2000 Server:



| Nome comum                                                                    |
|--------------------------------------------------------------------------------|
| [**Abandonar-replicação**](r-abandon-replication.md)                           |
| [**Coleta de lixo**](r-do-garbage-collection.md)                       |
| [**Recalcular-hierarquia**](r-recalculate-hierarchy.md)                       |
| [**Allocate-RIDs**](r-allocate-rids.md)                                       |
| [**Recalcular-segurança-herança**](r-recalculate-security-inheritance.md) |
| [**DS-verificação-obsoleto-fantasmas**](r-ds-check-stale-phantoms.md)                   |



## <a name="windows-server-2003"></a>Windows Server 2003

-   [Atributos](#windows-server-2003-attributes)
-   [Direitos estendidos](#windows-server-2003-extended-rights)



| Entrada | Valor |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | True                                                                                         |
| Object-Category             | 1                                                                                            |
| Categoria de objeto-padrão     | \-                                                                                           |
| Governs-Id                  | 1.2.840.113556.1.5.7000.47                                                                   |
| Padrão-ocultando valor        | 1                                                                                            |
| RDN-ATT-ID                  | [**Nome comum**](a-cn.md)<br/>                                                       |
| Subclasse de                 | [**Aplicativo-configurações**](c-applicationsettings.md)<br/>                             |
| Superiores possíveis          | [**Organização do servidor**](c-server.md)[](c-organization.md)                             |
| Classes Auxiliares           | \-                                                                                           |
| NT-Security-Descriptor      | O:BAG: INADEQUADO: S:                                                                                 |
| Descritor de segurança padrão | D: (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A;; RPLCLORC;;; AU |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2003-attributes"></a>Atributos do Windows Server 2003

Essa classe contém os seguintes atributos para o Windows Server 2003:



| Atributo                                                                   | Obrigatório | Derivado de                                                     |
|-----------------------------------------------------------------------------|-----------|------------------------------------------------------------------|
| [**Descrição do administrador**](a-admindescription.md)                             | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Administração – nome de exibição**](a-admindisplayname.md)                            | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Atributos permitidos**](a-allowedattributes.md)                           | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Permitido-atributos-efetivos**](a-allowedattributeseffective.md)        | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Classes filho permitidas**](a-allowedchildclasses.md)                      | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Permitido-filho-classes-efetivas**](a-allowedchildclasseseffective.md)   | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Nome do aplicativo**](a-applicationname.md)                               | Falso     | [**Aplicativo-configurações**](c-applicationsettings.md)<br/> |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)               | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Nome canônico**](a-canonicalname.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Nome comum**](a-cn.md)                                                 | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Criação-carimbo de data/hora**](a-createtimestamp.md)                              | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Descrição**](a-description.md)                                        | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Nome de exibição**](a-displayname.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Nome de exibição-imprimível**](a-displaynameprintable.md)                    | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**DMD-local**](a-dmdlocation.md)                                       | Falso     | **NTDS-DSA**                                                     |
| [**DSA-assinatura**](a-dsasignature.md)                                     | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**DS-Core-propagação-data**](a-dscorepropagationdata.md)                 | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Nome da extensão**](a-extensionname.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Flags**](a-flags.md)                                                    | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**De entrada**](a-fromentry.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**FRS-member-Reference-BL**](a-frsmemberreferencebl.md)                   | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**FRS-raiz-caminho**](a-frsrootpath.md)                                      | Falso     | **NTDS-DSA**                                                     |
| [**FSMO-função-proprietário**](a-fsmoroleowner.md)                                  | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Tem-mestre-NCs**](a-hasmasterncs.md)                                    | Falso     | **NTDS-DSA**                                                     |
| [**De-parcial-réplica-NCs**](a-haspartialreplicancs.md)                   | Falso     | **NTDS-DSA**                                                     |
| [**Tipo de instância**](a-instancetype.md)                                     | True      | [**Início**](c-top.md)<br/>                                  |
| [**ID de invocação**](a-invocationid.md)                                     | Falso     | **NTDS-DSA**                                                     |
| [**É-crítico-System-Object**](a-iscriticalsystemobject.md)               | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**É excluído**](a-isdeleted.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Is-member-of-DL**](a-memberof.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**É com proprietário de privilégio**](a-isprivilegeholder.md)                          | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Último backup-tempo de restauração**](a-lastbackuprestorationtime.md)         | Falso     | **NTDS-DSA**                                                     |
| [**Último-pai conhecido**](a-lastknownparent.md)                              | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Gerenciado por**](a-managedby.md)                                           | Falso     | **NTDS-DSA**                                                     |
| [**Objetos gerenciados**](a-managedobjects.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Mestre por**](a-masteredby.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Modificar-carimbo de data/hora**](a-modifytimestamp.md)                              | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                 | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**MS-COM-userlink**](a-mscom-userlink.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-aprox-immed-subordinados**](a-msds-approx-immed-subordinates.md) | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-Behavior-versão**](a-msds-behavior-version.md)                   | Falso     | **NTDS-DSA**                                                     |
| [**MS-DS-Consistency-filho-Count**](a-ms-ds-consistencychildcount.md)      | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-is-Domain-NCs**](a-msds-hasdomainncs.md)                         | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-tem-NCs-instanciáveis**](a-msds-hasinstantiatedncs.md)             | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-tem-mestre-NCs**](a-msds-hasmasterncs.md)                         | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-Masterd-by**](a-msds-masteredby.md)                              | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-Members-for-AZ-role-BL**](a-msds-membersforazrolebl.md)           | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-NC-repl-cursores**](a-msds-ncreplcursors.md)                       | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-NC-repl-Neighbors-Bounds**](a-msds-ncreplinboundneighbors.md)    | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-NC-repl-Bound-Neighbors**](a-msds-ncreploutboundneighbors.md)  | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-non-members-BL**](a-msds-nonmembersbl.md)                         | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)               | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-Operations-for-AZ-role-BL**](a-msds-operationsforazrolebl.md)     | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)     | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-repl-Attribute-meta-data**](a-msds-replattributemetadata.md)      | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-ReplicationEpoch**](a-msds-replicationepoch.md)                   | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-repl-Value-meta-data**](a-msds-replvaluemetadata.md)              | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-aposentado-repl-NC-Signatures**](a-msds-retiredreplncsignatures.md)  | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-Settings**](a-msds-settings.md)                                   | Falso     | [**Aplicativo-configurações**](c-applicationsettings.md)<br/> |
| [**ms-DS-Tasks-for-AZ-role-BL**](a-msds-tasksforazrolebl.md)               | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)               | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Ms-Exch-Owner-BL**](a-ownerbl.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                    | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Endereço de rede**](a-networkaddress.md)                                 | Falso     | **NTDS-DSA**                                                     |
| [**Não Security-Member-BL**](a-nonsecuritymemberbl.md)                     | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Lista de notificações**](a-notificationlist.md)                             | Falso     | [**Aplicativo-configurações**](c-applicationsettings.md)<br/> |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                    | True      | [**Início**](c-top.md)<br/>                                  |
| [**Obj-dist-Name**](a-distinguishedname.md)                                | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Objeto-categoria**](a-objectcategory.md)                                 | True      | [**Início**](c-top.md)<br/>                                  |
| [**Classe de objeto**](a-objectclass.md)                                       | True      | [**Início**](c-top.md)<br/>                                  |
| [**GUID do objeto**](a-objectguid.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Versão do objeto**](a-objectversion.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Opções**](a-options.md)                                                | Falso     | **NTDS-DSA**                                                     |
| [**Outros objetos bem conhecidos**](a-otherwellknownobjects.md)                 | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Parcial-atributo-exclusão-lista**](a-partialattributedeletionlist.md)   | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Conjunto de atributos parciais**](a-partialattributeset.md)                      | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Possíveis-inferiores**](a-possibleinferiors.md)                           | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Nome-do-objeto-proxy**](a-proxiedobjectname.md)                          | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Endereços de proxy**](a-proxyaddresses.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Consulta-política-BL**](a-querypolicybl.md)                                  | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Consulta-política-objeto**](a-querypolicyobject.md)                          | Falso     | **NTDS-DSA**                                                     |
| [**RDN**](a-name.md)                                                       | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Repl-Property-meta-data**](a-replpropertymetadata.md)                   | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Repl-UpToDate-vector**](a-repluptodatevector.md)                        | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Relatórios**](a-directreports.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Representantes-de**](a-repsfrom.md)                                             | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Reps-to**](a-repsto.md)                                                 | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Desativado-repl-DSA-Signatures**](a-retiredrepldsasignatures.md)           | Falso     | **NTDS-DSA**                                                     |
| [**Revisão**](a-revision.md)                                              | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**SD-direitos-efetivos**](a-sdrightseffective.md)                          | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Referência de servidor**](a-serverreference.md)                               | Falso     | **NTDS-DSA**                                                     |
| [**Servidor-referência-BL**](a-serverreferencebl.md)                          | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Mostrar-in-avançado-somente exibição**](a-showinadvancedviewonly.md)              | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Classe de objeto estrutural**](a-structuralobjectclass.md)                  | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Sub-referências**](a-subrefs.md)                                               | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Sinalizadores do sistema**](a-systemflags.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**USN-alterado**](a-usnchanged.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Criado pelo USN**](a-usncreated.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**USN-DSA-Last-obj-removido**](a-usndsalastobjremoved.md)                  | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**USN-entre sites**](a-usnintersite.md)                                     | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**USN-fonte**](a-usnsource.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**WBEM-caminho**](a-wbempath.md)                                             | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Objetos bem conhecidos**](a-wellknownobjects.md)                            | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Quando-alterado**](a-whenchanged.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Quando-criado**](a-whencreated.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**WWW-Home-Page**](a-wwwhomepage.md)                                      | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**WWW-página-outro**](a-url.md)                                             | Falso     | [**Início**](c-top.md)<br/>                                  |



## <a name="windows-server-2003-extended-rights"></a>Direitos estendidos do Windows Server 2003

Essa classe contém os seguintes direitos estendidos para o Windows Server 2003:



| Nome comum                                                                    |
|--------------------------------------------------------------------------------|
| [**Coleta de lixo**](r-do-garbage-collection.md)                       |
| [**Recalcular-hierarquia**](r-recalculate-hierarchy.md)                       |
| [**Allocate-RIDs**](r-allocate-rids.md)                                       |
| [**Recalcular-segurança-herança**](r-recalculate-security-inheritance.md) |
| [**DS-verificação-obsoleto-fantasmas**](r-ds-check-stale-phantoms.md)                   |
| [**Atualizar-grupo-cache**](r-refresh-group-cache.md)                           |



## <a name="adam"></a>ADAM

-   [Atributos](#adam-attributes)
-   [Direitos estendidos](#adam-extended-rights)



| Entrada | Valor |
|-----------------------------|------------------------------------------------------------------|
| System-Only                 | True                                                             |
| Object-Category             | 1                                                                |
| Categoria de objeto-padrão     | \-                                                               |
| Governs-Id                  | 1.2.840.113556.1.5.7000.47                                       |
| Padrão-ocultando valor        | 1                                                                |
| RDN-ATT-ID                  | [**Nome comum**](a-cn.md)<br/>                           |
| Subclasse de                 | [**Aplicativo-configurações**](c-applicationsettings.md)<br/> |
| Superiores possíveis          | [**Organização do servidor**](c-server.md)[](c-organization.md) |
| Classes Auxiliares           | \-                                                               |
| NT-Security-Descriptor      | O:BAG: INADEQUADO: S:                                                     |
| Descritor de segurança padrão | D:S:                                                             |
| System-Flags                | 0x00000010                                                       |



## <a name="adam-attributes"></a>Atributos do ADAM

Essa classe contém os seguintes atributos para ADAM:



| Atributo                                                                   | Obrigatório | Derivado de                                                     |
|-----------------------------------------------------------------------------|-----------|------------------------------------------------------------------|
| [**Descrição do administrador**](a-admindescription.md)                             | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Administração – nome de exibição**](a-admindisplayname.md)                            | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Atributos permitidos**](a-allowedattributes.md)                           | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Permitido-atributos-efetivos**](a-allowedattributeseffective.md)        | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Classes filho permitidas**](a-allowedchildclasses.md)                      | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Permitido-filho-classes-efetivas**](a-allowedchildclasseseffective.md)   | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)               | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Nome canônico**](a-canonicalname.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Nome comum**](a-cn.md)                                                 | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Criação-carimbo de data/hora**](a-createtimestamp.md)                              | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Descrição**](a-description.md)                                        | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Nome de exibição**](a-displayname.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**DMD-local**](a-dmdlocation.md)                                       | Falso     | **NTDS-DSA**                                                     |
| [**DSA-assinatura**](a-dsasignature.md)                                     | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**DS-Core-propagação-data**](a-dscorepropagationdata.md)                 | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**De entrada**](a-fromentry.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**FSMO-função-proprietário**](a-fsmoroleowner.md)                                  | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Tem-mestre-NCs**](a-hasmasterncs.md)                                    | Falso     | **NTDS-DSA**                                                     |
| [**De-parcial-réplica-NCs**](a-haspartialreplicancs.md)                   | Falso     | **NTDS-DSA**                                                     |
| [**Tipo de instância**](a-instancetype.md)                                     | True      | [**Início**](c-top.md)<br/>                                  |
| [**ID de invocação**](a-invocationid.md)                                     | Falso     | **NTDS-DSA**                                                     |
| [**É-crítico-System-Object**](a-iscriticalsystemobject.md)               | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**É excluído**](a-isdeleted.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Is-member-of-DL**](a-memberof.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Último backup-tempo de restauração**](a-lastbackuprestorationtime.md)         | Falso     | **NTDS-DSA**                                                     |
| [**Último-pai conhecido**](a-lastknownparent.md)                              | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Gerenciado por**](a-managedby.md)                                           | Falso     | **NTDS-DSA**                                                     |
| [**Objetos gerenciados**](a-managedobjects.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Mestre por**](a-masteredby.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Modificar-carimbo de data/hora**](a-modifytimestamp.md)                              | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-aprox-immed-subordinados**](a-msds-approx-immed-subordinates.md) | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-Behavior-versão**](a-msds-behavior-version.md)                   | Falso     | **NTDS-DSA**                                                     |
| [**MS-DS-Consistency-filho-Count**](a-ms-ds-consistencychildcount.md)      | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-Disable-for-instances-BL**](a-msds-disableforinstancesbl.md)      | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-is-Domain-NCs**](a-msds-hasdomainncs.md)                         | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-tem-NCs-instanciáveis**](a-msds-hasinstantiatedncs.md)             | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-tem-mestre-NCs**](a-msds-hasmasterncs.md)                         | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-Masterd-by**](a-msds-masteredby.md)                              | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-NC-repl-cursores**](a-msds-ncreplcursors.md)                       | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-NC-repl-Neighbors-Bounds**](a-msds-ncreplinboundneighbors.md)    | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-NC-repl-Bound-Neighbors**](a-msds-ncreploutboundneighbors.md)  | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-Port-LDAP**](a-msds-portldap.md)                                  | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-Port-SSL**](a-msds-portssl.md)                                    | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-repl-Attribute-meta-data**](a-msds-replattributemetadata.md)      | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-ReplicationEpoch**](a-msds-replicationepoch.md)                   | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-repl-Value-meta-data**](a-msds-replvaluemetadata.md)              | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-aposentado-repl-NC-Signatures**](a-msds-retiredreplncsignatures.md)  | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-Service-Account**](a-msds-serviceaccount.md)                      | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-Service-Account-BL**](a-msds-serviceaccountbl.md)                 | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-Service-Account-DNS-Domain**](a-msds-serviceaccountdnsdomain.md)  | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-Settings**](a-msds-settings.md)                                   | Falso     | [**Aplicativo-configurações**](c-applicationsettings.md)<br/> |
| [**Endereço de rede**](a-networkaddress.md)                                 | Falso     | **NTDS-DSA**                                                     |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                    | True      | [**Início**](c-top.md)<br/>                                  |
| [**Obj-dist-Name**](a-distinguishedname.md)                                | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Objeto-categoria**](a-objectcategory.md)                                 | True      | [**Início**](c-top.md)<br/>                                  |
| [**Classe de objeto**](a-objectclass.md)                                       | True      | [**Início**](c-top.md)<br/>                                  |
| [**GUID do objeto**](a-objectguid.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Versão do objeto**](a-objectversion.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Opções**](a-options.md)                                                | Falso     | **NTDS-DSA**                                                     |
| [**Outros objetos bem conhecidos**](a-otherwellknownobjects.md)                 | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Parcial-atributo-exclusão-lista**](a-partialattributedeletionlist.md)   | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Conjunto de atributos parciais**](a-partialattributeset.md)                      | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Possíveis-inferiores**](a-possibleinferiors.md)                           | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Nome-do-objeto-proxy**](a-proxiedobjectname.md)                          | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Endereços de proxy**](a-proxyaddresses.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Consulta-política-BL**](a-querypolicybl.md)                                  | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Consulta-política-objeto**](a-querypolicyobject.md)                          | Falso     | **NTDS-DSA**                                                     |
| [**RDN**](a-name.md)                                                       | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Repl-Property-meta-data**](a-replpropertymetadata.md)                   | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Repl-UpToDate-vector**](a-repluptodatevector.md)                        | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Representantes-de**](a-repsfrom.md)                                             | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Reps-to**](a-repsto.md)                                                 | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Desativado-repl-DSA-Signatures**](a-retiredrepldsasignatures.md)           | Falso     | **NTDS-DSA**                                                     |
| [**Revisão**](a-revision.md)                                              | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**SD-direitos-efetivos**](a-sdrightseffective.md)                          | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Referência de servidor**](a-serverreference.md)                               | Falso     | **NTDS-DSA**                                                     |
| [**Servidor-referência-BL**](a-serverreferencebl.md)                          | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Mostrar-in-avançado-somente exibição**](a-showinadvancedviewonly.md)              | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Classe de objeto estrutural**](a-structuralobjectclass.md)                  | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Sub-referências**](a-subrefs.md)                                               | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Sinalizadores do sistema**](a-systemflags.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**USN-alterado**](a-usnchanged.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Criado pelo USN**](a-usncreated.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**USN-DSA-Last-obj-removido**](a-usndsalastobjremoved.md)                  | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**USN-entre sites**](a-usnintersite.md)                                     | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**USN-fonte**](a-usnsource.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**WBEM-caminho**](a-wbempath.md)                                             | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Objetos bem conhecidos**](a-wellknownobjects.md)                            | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Quando-alterado**](a-whenchanged.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Quando-criado**](a-whencreated.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**WWW-Home-Page**](a-wwwhomepage.md)                                      | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**WWW-página-outro**](a-url.md)                                             | Falso     | [**Início**](c-top.md)<br/>                                  |



## <a name="adam-extended-rights"></a>Direitos estendidos do ADAM

Essa classe contém os seguintes direitos estendidos para o ADAM:



| Nome comum                                                                    |
|--------------------------------------------------------------------------------|
| [**Coleta de lixo**](r-do-garbage-collection.md)                       |
| [**Recalcular-segurança-herança**](r-recalculate-security-inheritance.md) |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2

-   [Atributos](#windows-server-2003-r2-attributes)
-   [Direitos estendidos](#windows-server-2003-r2-extended-rights)



| Entrada | Valor |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | True                                                                                         |
| Object-Category             | 1                                                                                            |
| Categoria de objeto-padrão     | \-                                                                                           |
| Governs-Id                  | 1.2.840.113556.1.5.7000.47                                                                   |
| Padrão-ocultando valor        | 1                                                                                            |
| RDN-ATT-ID                  | [**Nome comum**](a-cn.md)<br/>                                                       |
| Subclasse de                 | [**Aplicativo-configurações**](c-applicationsettings.md)<br/>                             |
| Superiores possíveis          | [**Organização do servidor**](c-server.md)[](c-organization.md)                             |
| Classes Auxiliares           | \-                                                                                           |
| NT-Security-Descriptor      | O:BAG: INADEQUADO: S:                                                                                 |
| Descritor de segurança padrão | D: (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A;; RPLCLORC;;; AU |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2003-r2-attributes"></a>Atributos do Windows Server 2003 R2

Essa classe contém os seguintes atributos para o Windows Server 2003 R2:



| Atributo                                                                   | Obrigatório | Derivado de                                                     |
|-----------------------------------------------------------------------------|-----------|------------------------------------------------------------------|
| [**Descrição do administrador**](a-admindescription.md)                             | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Administração – nome de exibição**](a-admindisplayname.md)                            | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Atributos permitidos**](a-allowedattributes.md)                           | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Permitido-atributos-efetivos**](a-allowedattributeseffective.md)        | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Classes filho permitidas**](a-allowedchildclasses.md)                      | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Permitido-filho-classes-efetivas**](a-allowedchildclasseseffective.md)   | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Nome do aplicativo**](a-applicationname.md)                               | Falso     | [**Aplicativo-configurações**](c-applicationsettings.md)<br/> |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)               | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Nome canônico**](a-canonicalname.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Nome comum**](a-cn.md)                                                 | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Criação-carimbo de data/hora**](a-createtimestamp.md)                              | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Descrição**](a-description.md)                                        | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Nome de exibição**](a-displayname.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Nome de exibição-imprimível**](a-displaynameprintable.md)                    | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**DMD-local**](a-dmdlocation.md)                                       | Falso     | **NTDS-DSA**                                                     |
| [**DSA-assinatura**](a-dsasignature.md)                                     | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**DS-Core-propagação-data**](a-dscorepropagationdata.md)                 | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Nome da extensão**](a-extensionname.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Flags**](a-flags.md)                                                    | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**De entrada**](a-fromentry.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**FRS-member-Reference-BL**](a-frsmemberreferencebl.md)                   | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**FRS-raiz-caminho**](a-frsrootpath.md)                                      | Falso     | **NTDS-DSA**                                                     |
| [**FSMO-função-proprietário**](a-fsmoroleowner.md)                                  | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Tem-mestre-NCs**](a-hasmasterncs.md)                                    | Falso     | **NTDS-DSA**                                                     |
| [**De-parcial-réplica-NCs**](a-haspartialreplicancs.md)                   | Falso     | **NTDS-DSA**                                                     |
| [**Tipo de instância**](a-instancetype.md)                                     | True      | [**Início**](c-top.md)<br/>                                  |
| [**ID de invocação**](a-invocationid.md)                                     | Falso     | **NTDS-DSA**                                                     |
| [**É-crítico-System-Object**](a-iscriticalsystemobject.md)               | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**É excluído**](a-isdeleted.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Is-member-of-DL**](a-memberof.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**É com proprietário de privilégio**](a-isprivilegeholder.md)                          | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Último backup-tempo de restauração**](a-lastbackuprestorationtime.md)         | Falso     | **NTDS-DSA**                                                     |
| [**Último-pai conhecido**](a-lastknownparent.md)                              | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Gerenciado por**](a-managedby.md)                                           | Falso     | **NTDS-DSA**                                                     |
| [**Objetos gerenciados**](a-managedobjects.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Mestre por**](a-masteredby.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Modificar-carimbo de data/hora**](a-modifytimestamp.md)                              | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                 | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**MS-COM-userlink**](a-mscom-userlink.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)         | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)             | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-aprox-immed-subordinados**](a-msds-approx-immed-subordinates.md) | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-Behavior-versão**](a-msds-behavior-version.md)                   | Falso     | **NTDS-DSA**                                                     |
| [**MS-DS-Consistency-filho-Count**](a-ms-ds-consistencychildcount.md)      | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-is-Domain-NCs**](a-msds-hasdomainncs.md)                         | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-tem-NCs-instanciáveis**](a-msds-hasinstantiatedncs.md)             | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-tem-mestre-NCs**](a-msds-hasmasterncs.md)                         | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-Masterd-by**](a-msds-masteredby.md)                              | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-Members-for-AZ-role-BL**](a-msds-membersforazrolebl.md)           | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-NC-repl-cursores**](a-msds-ncreplcursors.md)                       | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-NC-repl-Neighbors-Bounds**](a-msds-ncreplinboundneighbors.md)    | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-NC-repl-Bound-Neighbors**](a-msds-ncreploutboundneighbors.md)  | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-non-members-BL**](a-msds-nonmembersbl.md)                         | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)               | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-Operations-for-AZ-role-BL**](a-msds-operationsforazrolebl.md)     | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)     | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-repl-Attribute-meta-data**](a-msds-replattributemetadata.md)      | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-ReplicationEpoch**](a-msds-replicationepoch.md)                   | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-repl-Value-meta-data**](a-msds-replvaluemetadata.md)              | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-aposentado-repl-NC-Signatures**](a-msds-retiredreplncsignatures.md)  | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-Settings**](a-msds-settings.md)                                   | Falso     | [**Aplicativo-configurações**](c-applicationsettings.md)<br/> |
| [**ms-DS-Tasks-for-AZ-role-BL**](a-msds-tasksforazrolebl.md)               | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)               | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Ms-Exch-Owner-BL**](a-ownerbl.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**msSFU-30-POSIX-membro de**](a-mssfu30posixmemberof.md)                  | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                    | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Endereço de rede**](a-networkaddress.md)                                 | Falso     | **NTDS-DSA**                                                     |
| [**Não Security-Member-BL**](a-nonsecuritymemberbl.md)                     | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Lista de notificações**](a-notificationlist.md)                             | Falso     | [**Aplicativo-configurações**](c-applicationsettings.md)<br/> |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                    | True      | [**Início**](c-top.md)<br/>                                  |
| [**Obj-dist-Name**](a-distinguishedname.md)                                | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Objeto-categoria**](a-objectcategory.md)                                 | True      | [**Início**](c-top.md)<br/>                                  |
| [**Classe de objeto**](a-objectclass.md)                                       | True      | [**Início**](c-top.md)<br/>                                  |
| [**GUID do objeto**](a-objectguid.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Versão do objeto**](a-objectversion.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Opções**](a-options.md)                                                | Falso     | **NTDS-DSA**                                                     |
| [**Outros objetos bem conhecidos**](a-otherwellknownobjects.md)                 | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Parcial-atributo-exclusão-lista**](a-partialattributedeletionlist.md)   | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Conjunto de atributos parciais**](a-partialattributeset.md)                      | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Possíveis-inferiores**](a-possibleinferiors.md)                           | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Nome-do-objeto-proxy**](a-proxiedobjectname.md)                          | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Endereços de proxy**](a-proxyaddresses.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Consulta-política-BL**](a-querypolicybl.md)                                  | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Consulta-política-objeto**](a-querypolicyobject.md)                          | Falso     | **NTDS-DSA**                                                     |
| [**RDN**](a-name.md)                                                       | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Repl-Property-meta-data**](a-replpropertymetadata.md)                   | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Repl-UpToDate-vector**](a-repluptodatevector.md)                        | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Relatórios**](a-directreports.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Representantes-de**](a-repsfrom.md)                                             | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Reps-to**](a-repsto.md)                                                 | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Desativado-repl-DSA-Signatures**](a-retiredrepldsasignatures.md)           | Falso     | **NTDS-DSA**                                                     |
| [**Revisão**](a-revision.md)                                              | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**SD-direitos-efetivos**](a-sdrightseffective.md)                          | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Referência de servidor**](a-serverreference.md)                               | Falso     | **NTDS-DSA**                                                     |
| [**Servidor-referência-BL**](a-serverreferencebl.md)                          | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Mostrar-in-avançado-somente exibição**](a-showinadvancedviewonly.md)              | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Classe de objeto estrutural**](a-structuralobjectclass.md)                  | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Sub-referências**](a-subrefs.md)                                               | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Sinalizadores do sistema**](a-systemflags.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**USN-alterado**](a-usnchanged.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Criado pelo USN**](a-usncreated.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**USN-DSA-Last-obj-removido**](a-usndsalastobjremoved.md)                  | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**USN-entre sites**](a-usnintersite.md)                                     | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**USN-fonte**](a-usnsource.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**WBEM-caminho**](a-wbempath.md)                                             | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Objetos bem conhecidos**](a-wellknownobjects.md)                            | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Quando-alterado**](a-whenchanged.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Quando-criado**](a-whencreated.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**WWW-Home-Page**](a-wwwhomepage.md)                                      | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**WWW-página-outro**](a-url.md)                                             | Falso     | [**Início**](c-top.md)<br/>                                  |



## <a name="windows-server-2003-r2-extended-rights"></a>Direitos estendidos do Windows Server 2003 R2

Essa classe contém os seguintes direitos estendidos para o Windows Server 2003 R2:



| Nome comum                                                                    |
|--------------------------------------------------------------------------------|
| [**Coleta de lixo**](r-do-garbage-collection.md)                       |
| [**Recalcular-hierarquia**](r-recalculate-hierarchy.md)                       |
| [**Allocate-RIDs**](r-allocate-rids.md)                                       |
| [**Recalcular-segurança-herança**](r-recalculate-security-inheritance.md) |
| [**DS-verificação-obsoleto-fantasmas**](r-ds-check-stale-phantoms.md)                   |
| [**Atualizar-grupo-cache**](r-refresh-group-cache.md)                           |



## <a name="windows-server-2008"></a>Windows Server 2008

-   [Atributos](#windows-server-2008-attributes)
-   [Direitos estendidos](#windows-server-2008-extended-rights)



| Entrada | Valor |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | True                                                                                         |
| Object-Category             | 1                                                                                            |
| Categoria de objeto-padrão     | \-                                                                                           |
| Governs-Id                  | 1.2.840.113556.1.5.7000.47                                                                   |
| Padrão-ocultando valor        | 1                                                                                            |
| RDN-ATT-ID                  | [**Nome comum**](a-cn.md)<br/>                                                       |
| Subclasse de                 | [**Aplicativo-configurações**](c-applicationsettings.md)<br/>                             |
| Superiores possíveis          | [**Organização do servidor**](c-server.md)[](c-organization.md)                             |
| Classes Auxiliares           | \-                                                                                           |
| NT-Security-Descriptor      | O:BAG: INADEQUADO: S:                                                                                 |
| Descritor de segurança padrão | D: (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A;; RPLCLORC;;; AU |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2008-attributes"></a>Atributos do Windows Server 2008

Essa classe contém os seguintes atributos para o Windows Server 2008:



| Atributo                                                                      | Obrigatório | Derivado de                                                     |
|--------------------------------------------------------------------------------|-----------|------------------------------------------------------------------|
| [**Descrição do administrador**](a-admindescription.md)                                | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Administração – nome de exibição**](a-admindisplayname.md)                               | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Atributos permitidos**](a-allowedattributes.md)                              | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Permitido-atributos-efetivos**](a-allowedattributeseffective.md)           | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Classes filho permitidas**](a-allowedchildclasses.md)                         | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Permitido-filho-classes-efetivas**](a-allowedchildclasseseffective.md)      | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Nome do aplicativo**](a-applicationname.md)                                  | Falso     | [**Aplicativo-configurações**](c-applicationsettings.md)<br/> |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                  | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Nome canônico**](a-canonicalname.md)                                      | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Nome comum**](a-cn.md)                                                    | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Criação-carimbo de data/hora**](a-createtimestamp.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Descrição**](a-description.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Nome de exibição**](a-displayname.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Nome de exibição-imprimível**](a-displaynameprintable.md)                       | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**DMD-local**](a-dmdlocation.md)                                          | Falso     | **NTDS-DSA**                                                     |
| [**DSA-assinatura**](a-dsasignature.md)                                        | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**DS-Core-propagação-data**](a-dscorepropagationdata.md)                    | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Nome da extensão**](a-extensionname.md)                                      | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Flags**](a-flags.md)                                                       | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**De entrada**](a-fromentry.md)                                              | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                  | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**FRS-member-Reference-BL**](a-frsmemberreferencebl.md)                      | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**FRS-raiz-caminho**](a-frsrootpath.md)                                         | Falso     | **NTDS-DSA**                                                     |
| [**FSMO-função-proprietário**](a-fsmoroleowner.md)                                     | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Tem-mestre-NCs**](a-hasmasterncs.md)                                       | Falso     | **NTDS-DSA**                                                     |
| [**De-parcial-réplica-NCs**](a-haspartialreplicancs.md)                      | Falso     | **NTDS-DSA**                                                     |
| [**Tipo de instância**](a-instancetype.md)                                        | True      | [**Início**](c-top.md)<br/>                                  |
| [**ID de invocação**](a-invocationid.md)                                        | Falso     | **NTDS-DSA**                                                     |
| [**É-crítico-System-Object**](a-iscriticalsystemobject.md)                  | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**É excluído**](a-isdeleted.md)                                              | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Is-member-of-DL**](a-memberof.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**É com proprietário de privilégio**](a-isprivilegeholder.md)                             | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Último backup-tempo de restauração**](a-lastbackuprestorationtime.md)            | Falso     | **NTDS-DSA**                                                     |
| [**Último-pai conhecido**](a-lastknownparent.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Gerenciado por**](a-managedby.md)                                              | Falso     | **NTDS-DSA**                                                     |
| [**Objetos gerenciados**](a-managedobjects.md)                                    | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Mestre por**](a-masteredby.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Modificar-carimbo de data/hora**](a-modifytimestamp.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                    | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**MS-COM-userlink**](a-mscom-userlink.md)                                    | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)            | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-aprox-immed-subordinados**](a-msds-approx-immed-subordinates.md)    | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md) | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-Behavior-versão**](a-msds-behavior-version.md)                      | Falso     | **NTDS-DSA**                                                     |
| [**MS-DS-Consistency-filho-Count**](a-ms-ds-consistencychildcount.md)         | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                      | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-is-Domain-NCs**](a-msds-hasdomainncs.md)                            | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-tem-total de réplica-NCs**](a-msds-hasfullreplicancs.md)                 | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-tem-NCs-instanciáveis**](a-msds-hasinstantiatedncs.md)                | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-tem-mestre-NCs**](a-msds-hasmasterncs.md)                            | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-is-domain-for**](a-msds-isdomainfor.md)                              | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-is-full-Replica-for**](a-msds-isfullreplicafor.md)                   | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-isGC**](a-msds-isgc.md)                                              | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-is-partial-Replica-for**](a-msds-ispartialreplicafor.md)             | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-isRODC**](a-msds-isrodc.md)                                          | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-is-User-armazenável-at-RODC**](a-msds-isusercachableatrodc.md)          | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-KrbTgt-link-BL**](a-msds-krbtgtlinkbl.md)                            | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-Masterd-by**](a-msds-masteredby.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-Members-for-AZ-role-BL**](a-msds-membersforazrolebl.md)              | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-NC-repl-cursores**](a-msds-ncreplcursors.md)                          | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-NC-repl-Neighbors-Bounds**](a-msds-ncreplinboundneighbors.md)       | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-NC-repl-Bound-Neighbors**](a-msds-ncreploutboundneighbors.md)     | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)  | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Tipo ms-DS-NC**](a-msds-nctype.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-Never-Reveal-Group**](a-msds-neverrevealgroup.md)                    | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-non-members-BL**](a-msds-nonmembersbl.md)                            | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                  | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-Operations-for-AZ-role-BL**](a-msds-operationsforazrolebl.md)        | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)        | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-principal-Name**](a-msds-principalname.md)                           | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-PSO-aplicado**](a-msds-psoapplied.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-repl-Attribute-meta-data**](a-msds-replattributemetadata.md)         | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-ReplicationEpoch**](a-msds-replicationepoch.md)                      | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-repl-Value-meta-data**](a-msds-replvaluemetadata.md)                 | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-aposentado-repl-NC-Signatures**](a-msds-retiredreplncsignatures.md)     | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-revelados-DSAs**](a-msds-revealeddsas.md)                             | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-revelado-List-BL**](a-msds-revealedlistbl.md)                        | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-revelado-usuários**](a-msds-revealedusers.md)                           | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-Reveal-OnDemand-Group**](a-msds-revealondemandgroup.md)              | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-Settings**](a-msds-settings.md)                                      | Falso     | [**Aplicativo-configurações**](c-applicationsettings.md)<br/> |
| [**ms-DS-SiteName**](a-msds-sitename.md)                                      | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-Tasks-for-AZ-role-BL**](a-msds-tasksforazrolebl.md)                  | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                  | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Ms-Exch-Owner-BL**](a-ownerbl.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**msSFU-30-POSIX-membro de**](a-mssfu30posixmemberof.md)                     | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Endereço de rede**](a-networkaddress.md)                                    | Falso     | **NTDS-DSA**                                                     |
| [**Não Security-Member-BL**](a-nonsecuritymemberbl.md)                        | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Lista de notificações**](a-notificationlist.md)                                | Falso     | [**Aplicativo-configurações**](c-applicationsettings.md)<br/> |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                       | True      | [**Início**](c-top.md)<br/>                                  |
| [**Obj-dist-Name**](a-distinguishedname.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Objeto-categoria**](a-objectcategory.md)                                    | True      | [**Início**](c-top.md)<br/>                                  |
| [**Classe de objeto**](a-objectclass.md)                                          | True      | [**Início**](c-top.md)<br/>                                  |
| [**GUID do objeto**](a-objectguid.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Versão do objeto**](a-objectversion.md)                                      | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Opções**](a-options.md)                                                   | Falso     | **NTDS-DSA**                                                     |
| [**Outros objetos bem conhecidos**](a-otherwellknownobjects.md)                    | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Parcial-atributo-exclusão-lista**](a-partialattributedeletionlist.md)      | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Conjunto de atributos parciais**](a-partialattributeset.md)                         | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Possíveis-inferiores**](a-possibleinferiors.md)                              | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Nome-do-objeto-proxy**](a-proxiedobjectname.md)                             | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Endereços de proxy**](a-proxyaddresses.md)                                    | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Consulta-política-BL**](a-querypolicybl.md)                                     | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Consulta-política-objeto**](a-querypolicyobject.md)                             | Falso     | **NTDS-DSA**                                                     |
| [**RDN**](a-name.md)                                                          | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Repl-Property-meta-data**](a-replpropertymetadata.md)                      | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Repl-UpToDate-vector**](a-repluptodatevector.md)                           | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Relatórios**](a-directreports.md)                                             | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Representantes-de**](a-repsfrom.md)                                                | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Reps-to**](a-repsto.md)                                                    | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Desativado-repl-DSA-Signatures**](a-retiredrepldsasignatures.md)              | Falso     | **NTDS-DSA**                                                     |
| [**Revisão**](a-revision.md)                                                 | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**SD-direitos-efetivos**](a-sdrightseffective.md)                             | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Referência de servidor**](a-serverreference.md)                                  | Falso     | **NTDS-DSA**                                                     |
| [**Servidor-referência-BL**](a-serverreferencebl.md)                             | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Mostrar-in-avançado-somente exibição**](a-showinadvancedviewonly.md)                 | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Site-Object-BL**](a-siteobjectbl.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Classe de objeto estrutural**](a-structuralobjectclass.md)                     | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Sub-referências**](a-subrefs.md)                                                  | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                               | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Sinalizadores do sistema**](a-systemflags.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**USN-alterado**](a-usnchanged.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Criado pelo USN**](a-usncreated.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**USN-DSA-Last-obj-removido**](a-usndsalastobjremoved.md)                     | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**USN-entre sites**](a-usnintersite.md)                                        | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                    | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**USN-fonte**](a-usnsource.md)                                              | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**WBEM-caminho**](a-wbempath.md)                                                | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Objetos bem conhecidos**](a-wellknownobjects.md)                               | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Quando-alterado**](a-whenchanged.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Quando-criado**](a-whencreated.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**WWW-Home-Page**](a-wwwhomepage.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**WWW-página-outro**](a-url.md)                                                | Falso     | [**Início**](c-top.md)<br/>                                  |



## <a name="windows-server-2008-extended-rights"></a>Direitos estendidos do Windows Server 2008

Essa classe contém os seguintes direitos estendidos para o Windows Server 2008:



| Nome comum                                                                    |
|--------------------------------------------------------------------------------|
| [**Coleta de lixo**](r-do-garbage-collection.md)                       |
| [**Recalcular-hierarquia**](r-recalculate-hierarchy.md)                       |
| [**Allocate-RIDs**](r-allocate-rids.md)                                       |
| [**Recalcular-segurança-herança**](r-recalculate-security-inheritance.md) |
| [**DS-verificação-obsoleto-fantasmas**](r-ds-check-stale-phantoms.md)                   |
| [**Atualizar-grupo-cache**](r-refresh-group-cache.md)                           |
| [**Recarregar-SSL-certificado**](r-reload-ssl-certificate.md)                     |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2

-   [Atributos](#windows-server-2008-r2-attributes)
-   [Direitos estendidos](#windows-server-2008-r2-extended-rights)



| Entrada | Valor |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | True                                                                                         |
| Object-Category             | 1                                                                                            |
| Categoria de objeto-padrão     | \-                                                                                           |
| Governs-Id                  | 1.2.840.113556.1.5.7000.47                                                                   |
| Padrão-ocultando valor        | 1                                                                                            |
| RDN-ATT-ID                  | [**Nome comum**](a-cn.md)<br/>                                                       |
| Subclasse de                 | [**Aplicativo-configurações**](c-applicationsettings.md)<br/>                             |
| Superiores possíveis          | [**Organização do servidor**](c-server.md)[](c-organization.md)                             |
| Classes Auxiliares           | \-                                                                                           |
| NT-Security-Descriptor      | O:BAG: INADEQUADO: S:                                                                                 |
| Descritor de segurança padrão | D: (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A;; RPLCLORC;;; AU |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2008-r2-attributes"></a>Atributos do Windows Server 2008 R2

Essa classe contém os seguintes atributos para o Windows Server 2008 R2:



| Atributo                                                                        | Obrigatório | Derivado de                                                     |
|----------------------------------------------------------------------------------|-----------|------------------------------------------------------------------|
| [**Descrição do administrador**](a-admindescription.md)                                  | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Administração – nome de exibição**](a-admindisplayname.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Atributos permitidos**](a-allowedattributes.md)                                | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Permitido-atributos-efetivos**](a-allowedattributeseffective.md)             | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Classes filho permitidas**](a-allowedchildclasses.md)                           | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Permitido-filho-classes-efetivas**](a-allowedchildclasseseffective.md)        | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Nome do aplicativo**](a-applicationname.md)                                    | Falso     | [**Aplicativo-configurações**](c-applicationsettings.md)<br/> |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                    | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Nome canônico**](a-canonicalname.md)                                        | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Nome comum**](a-cn.md)                                                      | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Criação-carimbo de data/hora**](a-createtimestamp.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Descrição**](a-description.md)                                             | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Nome de exibição**](a-displayname.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Nome de exibição-imprimível**](a-displaynameprintable.md)                         | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**DMD-local**](a-dmdlocation.md)                                            | Falso     | **NTDS-DSA**                                                     |
| [**DSA-assinatura**](a-dsasignature.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**DS-Core-propagação-data**](a-dscorepropagationdata.md)                      | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Nome da extensão**](a-extensionname.md)                                        | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Flags**](a-flags.md)                                                         | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**De entrada**](a-fromentry.md)                                                | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                    | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**FRS-member-Reference-BL**](a-frsmemberreferencebl.md)                        | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**FRS-raiz-caminho**](a-frsrootpath.md)                                           | Falso     | **NTDS-DSA**                                                     |
| [**FSMO-função-proprietário**](a-fsmoroleowner.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Tem-mestre-NCs**](a-hasmasterncs.md)                                         | Falso     | **NTDS-DSA**                                                     |
| [**De-parcial-réplica-NCs**](a-haspartialreplicancs.md)                        | Falso     | **NTDS-DSA**                                                     |
| [**Tipo de instância**](a-instancetype.md)                                          | True      | [**Início**](c-top.md)<br/>                                  |
| [**ID de invocação**](a-invocationid.md)                                          | Falso     | **NTDS-DSA**                                                     |
| [**É-crítico-System-Object**](a-iscriticalsystemobject.md)                    | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**É excluído**](a-isdeleted.md)                                                | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Is-member-of-DL**](a-memberof.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**É com proprietário de privilégio**](a-isprivilegeholder.md)                               | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**É reciclado**](a-isrecycled.md)                                              | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Último backup-tempo de restauração**](a-lastbackuprestorationtime.md)              | Falso     | **NTDS-DSA**                                                     |
| [**Último-pai conhecido**](a-lastknownparent.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Gerenciado por**](a-managedby.md)                                                | Falso     | **NTDS-DSA**                                                     |
| [**Objetos gerenciados**](a-managedobjects.md)                                      | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Mestre por**](a-masteredby.md)                                              | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Modificar-carimbo de data/hora**](a-modifytimestamp.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                      | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**MS-COM-userlink**](a-mscom-userlink.md)                                      | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)              | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                  | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-aprox-immed-subordinados**](a-msds-approx-immed-subordinates.md)      | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)   | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-Behavior-versão**](a-msds-behavior-version.md)                        | Falso     | **NTDS-DSA**                                                     |
| [**MS-DS-Consistency-filho-Count**](a-ms-ds-consistencychildcount.md)           | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                        | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-habilitado-recurso**](a-msds-enabledfeature.md)                           | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-habilitado-Feature-BL**](a-msds-enabledfeaturebl.md)                      | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-is-Domain-NCs**](a-msds-hasdomainncs.md)                              | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-tem-total de réplica-NCs**](a-msds-hasfullreplicancs.md)                   | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-tem-NCs-instanciáveis**](a-msds-hasinstantiatedncs.md)                  | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-tem-mestre-NCs**](a-msds-hasmasterncs.md)                              | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)             | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-is-domain-for**](a-msds-isdomainfor.md)                                | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-is-full-Replica-for**](a-msds-isfullreplicafor.md)                     | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-isGC**](a-msds-isgc.md)                                                | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-is-partial-Replica-for**](a-msds-ispartialreplicafor.md)               | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-isRODC**](a-msds-isrodc.md)                                            | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-is-User-armazenável-at-RODC**](a-msds-isusercachableatrodc.md)            | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-KrbTgt-link-BL**](a-msds-krbtgtlinkbl.md)                              | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                              | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-local-efetivo-hora de exclusão**](a-msds-localeffectivedeletiontime.md) | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-local-efetivo-recicl-time**](a-msds-localeffectiverecycletime.md)   | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-Masterd-by**](a-msds-masteredby.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-Members-for-AZ-role-BL**](a-msds-membersforazrolebl.md)                | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-NC-repl-cursores**](a-msds-ncreplcursors.md)                            | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-NC-repl-Neighbors-Bounds**](a-msds-ncreplinboundneighbors.md)         | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-NC-repl-Bound-Neighbors**](a-msds-ncreploutboundneighbors.md)       | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)    | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Tipo ms-DS-NC**](a-msds-nctype.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-Never-Reveal-Group**](a-msds-neverrevealgroup.md)                      | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-non-members-BL**](a-msds-nonmembersbl.md)                              | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                    | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-OIDToGroup-link-BL**](a-msds-oidtogrouplinkbl.md)                      | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-Operations-for-AZ-role-BL**](a-msds-operationsforazrolebl.md)          | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)          | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-principal-Name**](a-msds-principalname.md)                             | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-PSO-aplicado**](a-msds-psoapplied.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-repl-Attribute-meta-data**](a-msds-replattributemetadata.md)           | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-ReplicationEpoch**](a-msds-replicationepoch.md)                        | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-repl-Value-meta-data**](a-msds-replvaluemetadata.md)                   | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-aposentado-repl-NC-Signatures**](a-msds-retiredreplncsignatures.md)       | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-revelados-DSAs**](a-msds-revealeddsas.md)                               | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-revelado-List-BL**](a-msds-revealedlistbl.md)                          | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-revelado-usuários**](a-msds-revealedusers.md)                             | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-Reveal-OnDemand-Group**](a-msds-revealondemandgroup.md)                | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-Settings**](a-msds-settings.md)                                        | Falso     | [**Aplicativo-configurações**](c-applicationsettings.md)<br/> |
| [**ms-DS-SiteName**](a-msds-sitename.md)                                        | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-Tasks-for-AZ-role-BL**](a-msds-tasksforazrolebl.md)                    | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                    | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Ms-Exch-Owner-BL**](a-ownerbl.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**msSFU-30-POSIX-membro de**](a-mssfu30posixmemberof.md)                       | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Endereço de rede**](a-networkaddress.md)                                      | Falso     | **NTDS-DSA**                                                     |
| [**Não Security-Member-BL**](a-nonsecuritymemberbl.md)                          | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Lista de notificações**](a-notificationlist.md)                                  | Falso     | [**Aplicativo-configurações**](c-applicationsettings.md)<br/> |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                         | True      | [**Início**](c-top.md)<br/>                                  |
| [**Obj-dist-Name**](a-distinguishedname.md)                                     | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Objeto-categoria**](a-objectcategory.md)                                      | True      | [**Início**](c-top.md)<br/>                                  |
| [**Classe de objeto**](a-objectclass.md)                                            | True      | [**Início**](c-top.md)<br/>                                  |
| [**GUID do objeto**](a-objectguid.md)                                              | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Versão do objeto**](a-objectversion.md)                                        | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Opções**](a-options.md)                                                     | Falso     | **NTDS-DSA**                                                     |
| [**Outros objetos bem conhecidos**](a-otherwellknownobjects.md)                      | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Parcial-atributo-exclusão-lista**](a-partialattributedeletionlist.md)        | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Conjunto de atributos parciais**](a-partialattributeset.md)                           | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Possíveis-inferiores**](a-possibleinferiors.md)                                | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Nome-do-objeto-proxy**](a-proxiedobjectname.md)                               | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Endereços de proxy**](a-proxyaddresses.md)                                      | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Consulta-política-BL**](a-querypolicybl.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Consulta-política-objeto**](a-querypolicyobject.md)                               | Falso     | **NTDS-DSA**                                                     |
| [**RDN**](a-name.md)                                                            | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Repl-Property-meta-data**](a-replpropertymetadata.md)                        | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Repl-UpToDate-vector**](a-repluptodatevector.md)                             | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Relatórios**](a-directreports.md)                                               | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Representantes-de**](a-repsfrom.md)                                                  | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Reps-to**](a-repsto.md)                                                      | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Desativado-repl-DSA-Signatures**](a-retiredrepldsasignatures.md)                | Falso     | **NTDS-DSA**                                                     |
| [**Revisão**](a-revision.md)                                                   | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**SD-direitos-efetivos**](a-sdrightseffective.md)                               | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Referência de servidor**](a-serverreference.md)                                    | Falso     | **NTDS-DSA**                                                     |
| [**Servidor-referência-BL**](a-serverreferencebl.md)                               | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Mostrar-in-avançado-somente exibição**](a-showinadvancedviewonly.md)                   | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Site-Object-BL**](a-siteobjectbl.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Classe de objeto estrutural**](a-structuralobjectclass.md)                       | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Sub-referências**](a-subrefs.md)                                                    | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Sinalizadores do sistema**](a-systemflags.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**USN-alterado**](a-usnchanged.md)                                              | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Criado pelo USN**](a-usncreated.md)                                              | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**USN-DSA-Last-obj-removido**](a-usndsalastobjremoved.md)                       | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**USN-entre sites**](a-usnintersite.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                      | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**USN-fonte**](a-usnsource.md)                                                | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**WBEM-caminho**](a-wbempath.md)                                                  | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Objetos bem conhecidos**](a-wellknownobjects.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Quando-alterado**](a-whenchanged.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Quando-criado**](a-whencreated.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**WWW-Home-Page**](a-wwwhomepage.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**WWW-página-outro**](a-url.md)                                                  | Falso     | [**Início**](c-top.md)<br/>                                  |



## <a name="windows-server-2008-r2-extended-rights"></a>Direitos estendidos do Windows Server 2008 R2

Essa classe contém os seguintes direitos estendidos para o Windows Server 2008 R2:



| Nome comum                                                                    |
|--------------------------------------------------------------------------------|
| [**Coleta de lixo**](r-do-garbage-collection.md)                       |
| [**Recalcular-hierarquia**](r-recalculate-hierarchy.md)                       |
| [**Allocate-RIDs**](r-allocate-rids.md)                                       |
| [**Recalcular-segurança-herança**](r-recalculate-security-inheritance.md) |
| [**DS-verificação-obsoleto-fantasmas**](r-ds-check-stale-phantoms.md)                   |
| [**Atualizar-grupo-cache**](r-refresh-group-cache.md)                           |
| [**Recarregar-SSL-certificado**](r-reload-ssl-certificate.md)                     |



## <a name="windows-server-2012"></a>Windows Server 2012

-   [Atributos](#windows-server-2012-attributes)
-   [Direitos estendidos](#windows-server-2012-extended-rights)
-   [Gravações validadas](#windows-server-2012-validated-writes)



| Entrada | Valor |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | True                                                                                         |
| Object-Category             | 1                                                                                            |
| Categoria de objeto-padrão     | \-                                                                                           |
| Governs-Id                  | 1.2.840.113556.1.5.7000.47                                                                   |
| Padrão-ocultando valor        | 1                                                                                            |
| RDN-ATT-ID                  | [**Nome comum**](a-cn.md)<br/>                                                       |
| Subclasse de                 | [**Aplicativo-configurações**](c-applicationsettings.md)<br/>                             |
| Superiores possíveis          | [**Organização do servidor**](c-server.md)[](c-organization.md)                             |
| Classes Auxiliares           | \-                                                                                           |
| NT-Security-Descriptor      | O:BAG: INADEQUADO: S:                                                                                 |
| Descritor de segurança padrão | D: (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A;; RPLCLORC;;; AU |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2012-attributes"></a>Atributos do Windows Server 2012

Essa classe contém os seguintes atributos para o Windows Server 2012:



| Atributo                                                                                    | Obrigatório | Derivado de                                                     |
|----------------------------------------------------------------------------------------------|-----------|------------------------------------------------------------------|
| [**Descrição do administrador**](a-admindescription.md)                                              | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Administração – nome de exibição**](a-admindisplayname.md)                                             | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Atributos permitidos**](a-allowedattributes.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Permitido-atributos-efetivos**](a-allowedattributeseffective.md)                         | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Classes filho permitidas**](a-allowedchildclasses.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Permitido-filho-classes-efetivas**](a-allowedchildclasseseffective.md)                    | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Nome do aplicativo**](a-applicationname.md)                                                | Falso     | [**Aplicativo-configurações**](c-applicationsettings.md)<br/> |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                                | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Nome canônico**](a-canonicalname.md)                                                    | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Nome comum**](a-cn.md)                                                                  | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Criação-carimbo de data/hora**](a-createtimestamp.md)                                               | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Descrição**](a-description.md)                                                         | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Nome de exibição**](a-displayname.md)                                                        | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Nome de exibição-imprimível**](a-displaynameprintable.md)                                     | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**DMD-local**](a-dmdlocation.md)                                                        | Falso     | **NTDS-DSA**                                                     |
| [**DSA-assinatura**](a-dsasignature.md)                                                      | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**DS-Core-propagação-data**](a-dscorepropagationdata.md)                                  | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Nome da extensão**](a-extensionname.md)                                                    | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Flags**](a-flags.md)                                                                     | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**De entrada**](a-fromentry.md)                                                            | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                                | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**FRS-member-Reference-BL**](a-frsmemberreferencebl.md)                                    | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**FRS-raiz-caminho**](a-frsrootpath.md)                                                       | Falso     | **NTDS-DSA**                                                     |
| [**FSMO-função-proprietário**](a-fsmoroleowner.md)                                                   | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Tem-mestre-NCs**](a-hasmasterncs.md)                                                     | Falso     | **NTDS-DSA**                                                     |
| [**De-parcial-réplica-NCs**](a-haspartialreplicancs.md)                                    | Falso     | **NTDS-DSA**                                                     |
| [**Tipo de instância**](a-instancetype.md)                                                      | True      | [**Início**](c-top.md)<br/>                                  |
| [**ID de invocação**](a-invocationid.md)                                                      | Falso     | **NTDS-DSA**                                                     |
| [**É-crítico-System-Object**](a-iscriticalsystemobject.md)                                | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**É excluído**](a-isdeleted.md)                                                            | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Is-member-of-DL**](a-memberof.md)                                                        | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**É com proprietário de privilégio**](a-isprivilegeholder.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**É reciclado**](a-isrecycled.md)                                                          | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Último backup-tempo de restauração**](a-lastbackuprestorationtime.md)                          | Falso     | **NTDS-DSA**                                                     |
| [**Último-pai conhecido**](a-lastknownparent.md)                                               | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Gerenciado por**](a-managedby.md)                                                            | Falso     | **NTDS-DSA**                                                     |
| [**Objetos gerenciados**](a-managedobjects.md)                                                  | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Mestre por**](a-masteredby.md)                                                          | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Modificar-carimbo de data/hora**](a-modifytimestamp.md)                                               | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                                  | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**MS-COM-userlink**](a-mscom-userlink.md)                                                  | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)                          | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                              | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-aprox-immed-subordinados**](a-msds-approx-immed-subordinates.md)                  | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)               | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-Behavior-versão**](a-msds-behavior-version.md)                                    | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-Claim-shares-possíveis-Values-with-BL**](a-msds-claimsharespossiblevalueswithbl.md) | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**MS-DS-Consistency-filho-Count**](a-ms-ds-consistencychildcount.md)                       | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                                    | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-habilitado-recurso**](a-msds-enabledfeature.md)                                       | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-habilitado-Feature-BL**](a-msds-enabledfeaturebl.md)                                  | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-is-Domain-NCs**](a-msds-hasdomainncs.md)                                          | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-tem-total de réplica-NCs**](a-msds-hasfullreplicancs.md)                               | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-tem-NCs-instanciáveis**](a-msds-hasinstantiatedncs.md)                              | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-tem-mestre-NCs**](a-msds-hasmasterncs.md)                                          | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)                         | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-is-domain-for**](a-msds-isdomainfor.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-is-full-Replica-for**](a-msds-isfullreplicafor.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-isGC**](a-msds-isgc.md)                                                            | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-is-partial-Replica-for**](a-msds-ispartialreplicafor.md)                           | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-is-Primary-Computer-for**](a-msds-isprimarycomputerfor.md)                         | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-isRODC**](a-msds-isrodc.md)                                                        | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-is-User-armazenável-at-RODC**](a-msds-isusercachableatrodc.md)                        | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-KrbTgt-link-BL**](a-msds-krbtgtlinkbl.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-local-efetivo-hora de exclusão**](a-msds-localeffectivedeletiontime.md)             | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-local-efetivo-recicl-time**](a-msds-localeffectiverecycletime.md)               | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-Masterd-by**](a-msds-masteredby.md)                                               | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-Members-for-AZ-role-BL**](a-msds-membersforazrolebl.md)                            | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-Members-of-Resource-Property-List-BL**](a-msds-membersofresourcepropertylistbl.md) | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-NC-repl-cursores**](a-msds-ncreplcursors.md)                                        | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-NC-repl-Neighbors-Bounds**](a-msds-ncreplinboundneighbors.md)                     | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-NC-repl-Bound-Neighbors**](a-msds-ncreploutboundneighbors.md)                   | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)                | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Tipo ms-DS-NC**](a-msds-nctype.md)                                                       | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-Never-Reveal-Group**](a-msds-neverrevealgroup.md)                                  | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-non-members-BL**](a-msds-nonmembersbl.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                                | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-OIDToGroup-link-BL**](a-msds-oidtogrouplinkbl.md)                                  | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-Operations-for-AZ-role-BL**](a-msds-operationsforazrolebl.md)                      | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)                      | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-principal-Name**](a-msds-principalname.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-PSO-aplicado**](a-msds-psoapplied.md)                                               | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-repl-Attribute-meta-data**](a-msds-replattributemetadata.md)                       | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-ReplicationEpoch**](a-msds-replicationepoch.md)                                    | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-repl-Value-meta-data**](a-msds-replvaluemetadata.md)                               | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-aposentado-repl-NC-Signatures**](a-msds-retiredreplncsignatures.md)                   | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-revelados-DSAs**](a-msds-revealeddsas.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-revelado-List-BL**](a-msds-revealedlistbl.md)                                      | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-revelado-usuários**](a-msds-revealedusers.md)                                         | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-Reveal-OnDemand-Group**](a-msds-revealondemandgroup.md)                            | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-Settings**](a-msds-settings.md)                                                    | Falso     | [**Aplicativo-configurações**](c-applicationsettings.md)<br/> |
| [**ms-DS-SiteName**](a-msds-sitename.md)                                                    | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-Tasks-for-AZ-role-BL**](a-msds-tasksforazrolebl.md)                                | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                                | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-TDO-egresso-BL**](a-msds-tdoegressbl.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-TDO-ingress-BL**](a-msds-tdoingressbl.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**ms-DS-Value-Type-Reference-BL**](a-msds-valuetypereferencebl.md)                         | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Ms-Exch-Owner-BL**](a-ownerbl.md)                                                        | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**msSFU-30-POSIX-membro de**](a-mssfu30posixmemberof.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                                     | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Endereço de rede**](a-networkaddress.md)                                                  | Falso     | **NTDS-DSA**                                                     |
| [**Não Security-Member-BL**](a-nonsecuritymemberbl.md)                                      | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Lista de notificações**](a-notificationlist.md)                                              | Falso     | [**Aplicativo-configurações**](c-applicationsettings.md)<br/> |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                                     | True      | [**Início**](c-top.md)<br/>                                  |
| [**Obj-dist-Name**](a-distinguishedname.md)                                                 | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Objeto-categoria**](a-objectcategory.md)                                                  | True      | [**Início**](c-top.md)<br/>                                  |
| [**Classe de objeto**](a-objectclass.md)                                                        | True      | [**Início**](c-top.md)<br/>                                  |
| [**GUID do objeto**](a-objectguid.md)                                                          | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Versão do objeto**](a-objectversion.md)                                                    | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Opções**](a-options.md)                                                                 | Falso     | **NTDS-DSA**                                                     |
| [**Outros objetos bem conhecidos**](a-otherwellknownobjects.md)                                  | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Parcial-atributo-exclusão-lista**](a-partialattributedeletionlist.md)                    | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Conjunto de atributos parciais**](a-partialattributeset.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Possíveis-inferiores**](a-possibleinferiors.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Nome-do-objeto-proxy**](a-proxiedobjectname.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Endereços de proxy**](a-proxyaddresses.md)                                                  | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Consulta-política-BL**](a-querypolicybl.md)                                                   | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Consulta-política-objeto**](a-querypolicyobject.md)                                           | Falso     | **NTDS-DSA**                                                     |
| [**RDN**](a-name.md)                                                                        | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Repl-Property-meta-data**](a-replpropertymetadata.md)                                    | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Repl-UpToDate-vector**](a-repluptodatevector.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Relatórios**](a-directreports.md)                                                           | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Representantes-de**](a-repsfrom.md)                                                              | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Reps-to**](a-repsto.md)                                                                  | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Desativado-repl-DSA-Signatures**](a-retiredrepldsasignatures.md)                            | Falso     | **NTDS-DSA**                                                     |
| [**Revisão**](a-revision.md)                                                               | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**SD-direitos-efetivos**](a-sdrightseffective.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Referência de servidor**](a-serverreference.md)                                                | Falso     | **NTDS-DSA**                                                     |
| [**Servidor-referência-BL**](a-serverreferencebl.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Mostrar-in-avançado-somente exibição**](a-showinadvancedviewonly.md)                               | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Site-Object-BL**](a-siteobjectbl.md)                                                     | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Classe de objeto estrutural**](a-structuralobjectclass.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Sub-referências**](a-subrefs.md)                                                                | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                             | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Sinalizadores do sistema**](a-systemflags.md)                                                        | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**USN-alterado**](a-usnchanged.md)                                                          | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Criado pelo USN**](a-usncreated.md)                                                          | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**USN-DSA-Last-obj-removido**](a-usndsalastobjremoved.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**USN-entre sites**](a-usnintersite.md)                                                      | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                                  | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**USN-fonte**](a-usnsource.md)                                                            | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**WBEM-caminho**](a-wbempath.md)                                                              | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Objetos bem conhecidos**](a-wellknownobjects.md)                                             | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Quando-alterado**](a-whenchanged.md)                                                        | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**Quando-criado**](a-whencreated.md)                                                        | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**WWW-Home-Page**](a-wwwhomepage.md)                                                       | Falso     | [**Início**](c-top.md)<br/>                                  |
| [**WWW-página-outro**](a-url.md)                                                              | Falso     | [**Início**](c-top.md)<br/>                                  |



## <a name="windows-server-2012-extended-rights"></a>Direitos estendidos do Windows Server 2012

Essa classe contém os seguintes direitos estendidos para o Windows Server 2012:



| Nome comum                                                                    |
|--------------------------------------------------------------------------------|
| [**Coleta de lixo**](r-do-garbage-collection.md)                       |
| [**Recalcular-hierarquia**](r-recalculate-hierarchy.md)                       |
| [**Allocate-RIDs**](r-allocate-rids.md)                                       |
| [**Recalcular-segurança-herança**](r-recalculate-security-inheritance.md) |
| [**DS-verificação-obsoleto-fantasmas**](r-ds-check-stale-phantoms.md)                   |
| [**Atualizar-grupo-cache**](r-refresh-group-cache.md)                           |
| [**Recarregar-SSL-certificado**](r-reload-ssl-certificate.md)                     |



## <a name="windows-server-2012-validated-writes"></a>Gravações validadas do Windows Server 2012

Essa classe contém as seguintes gravações validadas para o Windows Server 2012:



| Nome comum                                                                    |
|--------------------------------------------------------------------------------|
| [**Validado-MS-DS-Behavior-versão**](r-validated-ms-ds-behavior-version.md) |



 

 





