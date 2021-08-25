---
title: Package-Flags atributo
description: Um campo de bits que contém os sinalizadores de estado de implantação para um aplicativo.
ms.assetid: 5b6cfed5-db04-438e-912b-60dce7a16409
ms.tgt_platform: multiple
keywords:
- Package-Flags atributo AD Schema
- Esquema do AD do atributo packageFlags
topic_type:
- apiref
api_name:
- Package-Flags
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd6965b5c39603032bdb673df10026b0eed2a5d5ae838aeb094013d9a5e95dff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119923936"
---
# <a name="package-flags-attribute"></a>Package-Flags atributo

Um campo de bits que contém os sinalizadores de estado de implantação para um aplicativo.

Esse atributo pode ser zero ou uma combinação de um ou mais dos valores a seguir.

| Valor                 | Descrição                                                                                                                                                                                                                                                                                                    |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x00000004<br/> | A versão nãomanageda desse aplicativo deve ser desinstalada antes da atribuição. **Windows XP com SP1 e posterior:** Não há suporte para esse sinalizador.<br/> <br/>                                                                                                                                          |
| 0x00000008<br/> | Este é um aplicativo publicado.<br/>                                                                                                                                                                                                                                                                    |
| 0x00000010<br/> | Esse pacote foi implantado após a Versão Beta 3 Windows 2000.<br/>                                                                                                                                                                                                                                             |
| 0x00000020<br/> | Esse aplicativo pode ser instalado com o **recurso Adicionar ou Remover Programas** do Painel de Controle.<br/>                                                                                                                                                                                                 |
| 0x00000040<br/> | Esse aplicativo pode ser instalado automaticamente sob demanda.<br/>                                                                                                                                                                                                                                                   |
| 0x00000080<br/> | Esse aplicativo é órfão. Um aplicativo publicado poderá ficar órfão se o administrador remover o aplicativo da lista de aplicativos implantáveis.<br/>                                                                                                                                    |
| 0x00000100<br/> | Esse aplicativo deve ser tratado como desinstalado.<br/>                                                                                                                                                                                                                                                  |
| 0x00000200<br/> | Esse aplicativo está disponível apenas como piloto.<br/>                                                                                                                                                                                                                                                      |
| 0x00000400<br/> | Este é um aplicativo atribuído. Um aplicativo atribuído não pode ser totalmente removido pelo usuário. Se o usuário tentar desinstalar o aplicativo com o recurso Adicionar ou Remover Programas do Painel de Controle, o aplicativo será anunciado novamente no computador quando a remoção for concluída. <br/> |
| 0x00000800<br/> | Esse aplicativo fica órfão quando a política é removida. Se o administrador remover a política relacionada a esse aplicativo, o administrador não controlará mais a implantação do aplicativo, mas o aplicativo instalado continuará funcionando.<br/>                          |
| 0x00001000<br/> | Esse aplicativo é desinstalado quando a política de implantação é removida.<br/>                                                                                                                                                                                                                              |
| 0x00002000<br/> | Uma instalação completa de aplicativos atribuídos ao usuário será executada.<br/>                                                                                                                                                                                                                                |
| 0x00004000<br/> | As versões mais antigas desse aplicativo devem ser atualizadas para esta versão.<br/>                                                                                                                                                                                                                                |
| 0x00008000<br/> | Esse pacote dá suporte apenas a uma interface mínima do usuário com uma barra de progresso para o processo de instalação.<br/>                                                                                                                                                                                               |
| 0x00010000<br/> | Este é um pacote para versões de 32 bits do Windows que não deve ser executado no Windows XP Professional x64 Edition ou em versões de 64 bits do Windows Server 2003.<br/>                                                                                                                                      |
| 0x00020000<br/> | Esse pacote é adequado para qualquer idioma.<br/>                                                                                                                                                                                                                                                          |
| 0x00040000<br/> | Este pacote tem atualizações.<br/>                                                                                                                                                                                                                                                                          |
| 0x00080000<br/> | Esse pacote tem uma interface do usuário completa para o processo de instalação.<br/>                                                                                                                                                                                                                                |
| 0x00100000<br/> | As classes para esse aplicativo serão preservadas durante uma operação de reimplantação se o aplicativo for reimplantado em um domínio renomeando.<br/>                                                                                                                                                                       |



 



| Entrada | Valor |
|-------------------|--------------------------------------|
| CN                | Package-Flags                        |
| Ldap-Display-Name | packageFlags                         |
| Tamanho              | \-                                   |
| Privilégio de atualização  | \-                                   |
| Frequência de atualização  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.327               |
| System-Id-Guid    | 7d6c0e99-7e20-11d0-afd6-00c04fd930c9 |
| Syntax            | [**Enumeração**](s-enumeration.md) |



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
| Tem valor único       | Verdadeiro                                                             |
| É indexado             | Verdadeiro                                                             |
| No Catálogo Global      | Falso                                                            |
| Descritor de segurança NT | O:BAG:BAD:S:                                                     |
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
| É de valor único       | Verdadeiro                                                             |
| É indexado             | Verdadeiro                                                             |
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
| É de valor único       | Verdadeiro                                                             |
| É indexado             | Verdadeiro                                                             |
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
| É de valor único       | Verdadeiro                                                             |
| É indexado             | Verdadeiro                                                             |
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
| É de valor único       | Verdadeiro                                                             |
| É indexado             | Verdadeiro                                                             |
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
| É de valor único       | Verdadeiro                                                             |
| É indexado             | Verdadeiro                                                             |
| No Catálogo Global      | Falso                                                            |
| Descritor de segurança NT | O:BAG:BAD:S:                                                     |
| Range-Lower            | \-                                                               |
| Range-Upper            | \-                                                               |
| Search-Flags           | 0x00000001                                                       |
| System-Flags           | 0x00000010                                                       |
| Classes usadas em        | [**Registro de pacote**](c-packageregistration.md)<br/> |



 

 





