---
title: Package-Flags atributo
description: Um campo de bits que contém os sinalizadores de estado de implantação de um aplicativo.
ms.assetid: 5b6cfed5-db04-438e-912b-60dce7a16409
ms.tgt_platform: multiple
keywords:
- Esquema de Package-Flags do atributo AD
- Esquema de AD do atributo packageFlags
topic_type:
- apiref
api_name:
- Package-Flags
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7202124bdeac22347d727638dc564a145599e9c7
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103645517"
---
# <a name="package-flags-attribute"></a>Package-Flags atributo

Um campo de bits que contém os sinalizadores de estado de implantação de um aplicativo.

Esse atributo pode ser zero ou uma combinação de um ou mais dos valores a seguir.

| Valor                 | Descrição                                                                                                                                                                                                                                                                                                    |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x00000004<br/> | A versão não gerenciada deste aplicativo deve ser desinstalada antes de atribuir. **Windows XP com SP1 e posterior:** Não há suporte para esse sinalizador.<br/> <br/>                                                                                                                                          |
| 0x00000008<br/> | Este é um aplicativo publicado.<br/>                                                                                                                                                                                                                                                                    |
| 0x00000010<br/> | Este pacote foi implantado após a versão beta 3 do Windows 2000.<br/>                                                                                                                                                                                                                                             |
| 0x00000020<br/> | Esse aplicativo pode ser instalado com o recurso **Adicionar ou remover programas** do painel de controle.<br/>                                                                                                                                                                                                 |
| 0x00000040<br/> | Esse aplicativo pode ser instalado automaticamente sob demanda.<br/>                                                                                                                                                                                                                                                   |
| 0x00000080<br/> | Este aplicativo está órfão. Um aplicativo publicado pode se tornar órfão se o administrador remover o aplicativo da lista de aplicativos implantáveis.<br/>                                                                                                                                    |
| 0x00000100<br/> | Esse aplicativo deve ser tratado como desinstalado.<br/>                                                                                                                                                                                                                                                  |
| 0x00000200<br/> | Este aplicativo está disponível apenas como um piloto.<br/>                                                                                                                                                                                                                                                      |
| 0x00000400<br/> | Este é um aplicativo atribuído. Um aplicativo atribuído não pode ser totalmente removido pelo usuário. Se o usuário tentar desinstalar o aplicativo com o recurso **Adicionar ou remover programas** do painel de controle, o aplicativo será anunciado novamente para o computador quando a remoção for concluída.<br/> |
| 0x00000800<br/> | Esse aplicativo fica órfão quando a política é removida. Se o administrador remover a política que está relacionada a esse aplicativo, o administrador não controlará mais a implantação do aplicativo, mas o aplicativo instalado continuará a funcionar.<br/>                          |
| 0x00001000<br/> | Esse aplicativo é desinstalado quando a política de implantação é removida.<br/>                                                                                                                                                                                                                              |
| 0x00002000<br/> | Uma instalação completa de aplicativos atribuídos pelo usuário será executada.<br/>                                                                                                                                                                                                                                |
| 0x00004000<br/> | Versões mais antigas deste aplicativo devem ser atualizadas para esta versão.<br/>                                                                                                                                                                                                                                |
| 0x00008000<br/> | Este pacote dá suporte apenas a uma interface de usuário mínima com uma barra de progresso para o processo de instalação.<br/>                                                                                                                                                                                               |
| 0x00010000<br/> | Este é um pacote para versões de 32 bits do Windows que não devem ser executadas no Windows XP Professional x64 Edition ou nas versões de 64 bits do Windows Server 2003.<br/>                                                                                                                                      |
| 0x00020000<br/> | Este pacote é adequado para qualquer idioma.<br/>                                                                                                                                                                                                                                                          |
| 0x00040000<br/> | Este pacote tem atualizações.<br/>                                                                                                                                                                                                                                                                          |
| 0x00080000<br/> | Este pacote tem uma interface de usuário completa para o processo de instalação.<br/>                                                                                                                                                                                                                                |
| 0x00100000<br/> | As classes desse aplicativo serão preservadas durante uma operação de reimplantação se o aplicativo for reimplantado em uma renomeação de domínio.<br/>                                                                                                                                                                       |



 



| Entrada | Valor |
|-------------------|--------------------------------------|
| CN                | Package-Flags                        |
| LDAP-Display-Name | packageFlags                         |
| Tamanho              | \-                                   |
| Privilégio de atualização  | \-                                   |
| Frequência de atualização  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.327               |
| System-ID-GUID    | 7d6c0e99-7e20-11d0-afd6-00c04fd930c9 |
| Sintaxe            | [**Enumeração**](s-enumeration.md) |



## <a name="implementations"></a>Implementações

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Valor |
|------------------------|------------------------------------------------------------------|
| ID do link                | \-                                                               |
| MAPI-Id                | \-                                                               |
| System-Only            | Falso                                                            |
| É de valor único       | True                                                             |
| É indexado             | True                                                             |
| No catálogo global      | Falso                                                            |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                     |
| Range-Lower            | \-                                                               |
| Range-Upper            | \-                                                               |
| Search-Flags           | 0x00000001                                                       |
| System-Flags           | 0x00000010                                                       |
| Classes usadas em        | [**Registro de pacote**](c-packageregistration.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|------------------------------------------------------------------|
| ID do link                | \-                                                               |
| MAPI-Id                | \-                                                               |
| System-Only            | Falso                                                            |
| É de valor único       | True                                                             |
| É indexado             | True                                                             |
| No catálogo global      | Falso                                                            |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                     |
| Range-Lower            | \-                                                               |
| Range-Upper            | \-                                                               |
| Search-Flags           | 0x00000001                                                       |
| System-Flags           | 0x00000010                                                       |
| Classes usadas em        | [**Registro de pacote**](c-packageregistration.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|------------------------------------------------------------------|
| ID do link                | \-                                                               |
| MAPI-Id                | \-                                                               |
| System-Only            | Falso                                                            |
| É de valor único       | True                                                             |
| É indexado             | True                                                             |
| No catálogo global      | Falso                                                            |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                     |
| Range-Lower            | \-                                                               |
| Range-Upper            | \-                                                               |
| Search-Flags           | 0x00000001                                                       |
| System-Flags           | 0x00000010                                                       |
| Classes usadas em        | [**Registro de pacote**](c-packageregistration.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|------------------------------------------------------------------|
| ID do link                | \-                                                               |
| MAPI-Id                | \-                                                               |
| System-Only            | Falso                                                            |
| É de valor único       | True                                                             |
| É indexado             | True                                                             |
| No catálogo global      | Falso                                                            |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                     |
| Range-Lower            | \-                                                               |
| Range-Upper            | \-                                                               |
| Search-Flags           | 0x00000001                                                       |
| System-Flags           | 0x00000010                                                       |
| Classes usadas em        | [**Registro de pacote**](c-packageregistration.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|------------------------------------------------------------------|
| ID do link                | \-                                                               |
| MAPI-Id                | \-                                                               |
| System-Only            | Falso                                                            |
| É de valor único       | True                                                             |
| É indexado             | True                                                             |
| No catálogo global      | Falso                                                            |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                     |
| Range-Lower            | \-                                                               |
| Range-Upper            | \-                                                               |
| Search-Flags           | 0x00000001                                                       |
| System-Flags           | 0x00000010                                                       |
| Classes usadas em        | [**Registro de pacote**](c-packageregistration.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|------------------------------------------------------------------|
| ID do link                | \-                                                               |
| MAPI-Id                | \-                                                               |
| System-Only            | Falso                                                            |
| É de valor único       | True                                                             |
| É indexado             | True                                                             |
| No catálogo global      | Falso                                                            |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                     |
| Range-Lower            | \-                                                               |
| Range-Upper            | \-                                                               |
| Search-Flags           | 0x00000001                                                       |
| System-Flags           | 0x00000010                                                       |
| Classes usadas em        | [**Registro de pacote**](c-packageregistration.md)<br/> |



 

 





