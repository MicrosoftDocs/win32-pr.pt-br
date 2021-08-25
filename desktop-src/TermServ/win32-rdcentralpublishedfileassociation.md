---
title: Classe Win32_RDCentralPublishedFileAssociation
description: Informações de uma extensão de arquivo associada a um aplicativo.
ms.assetid: ba12d933-572c-48d3-bf0f-1c99de61457d
ms.tgt_platform: multiple
keywords:
- Classe de Win32_RDCentralPublishedFileAssociation Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_RDCentralPublishedFileAssociation classe, descrita
topic_type:
- apiref
api_name:
- Win32_RDCentralPublishedFileAssociation
- Win32_RDCentralPublishedFileAssociation.ExtName
- Win32_RDCentralPublishedFileAssociation.AppAlias
- Win32_RDCentralPublishedFileAssociation.FarmAlias
- Win32_RDCentralPublishedFileAssociation.ProgIdHint
- Win32_RDCentralPublishedFileAssociation.IconContents
- Win32_RDCentralPublishedFileAssociation.PrimaryHandler
api_location:
- TscPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41361959c56810036b8ca2e17d338e2ff1d3433c6e0384fd168a2d21d6e0e0f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119868446"
---
# <a name="win32_rdcentralpublishedfileassociation-class"></a>\_Classe Win32 RDCentralPublishedFileAssociation

Informações para uma extensão de arquivo associada a um aplicativo

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[dynamic, provider("Win32_TSCentralPublisher_Prov")]
class Win32_RDCentralPublishedFileAssociation
{
  string  ExtName;
  string  AppAlias;
  string  FarmAlias;
  string  ProgIdHint;
  uint8   IconContents[];
  boolean PrimaryHandler;
};
```

## <a name="members"></a>Membros

A classe **Win32 \_ RDCentralPublishedFileAssociation** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Win32 \_ RDCentralPublishedFileAssociation** tem essas propriedades.

<dl> <dt>

**AppAlias**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Alias do RemoteApp da Associação de arquivo.

</dd> <dt>

**ExtName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nome da extensão (por exemplo, .txt).

</dd> <dt>

**FarmAlias**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Alias do farm RemoteApp's da Associação de arquivo

</dd> <dt>

**IconContents**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **uint8**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Conteúdo do ícone para esta associação de arquivo.

</dd> <dt>

**PrimaryHandler**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Reservado para uso futuro. Será sempre **verdadeiro**.

</dd> <dt>

**ProgIdHint**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Dica para ajudar a abrir documentos com essa associação de arquivo.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                           |
| Namespace<br/>                | \\TerminalServices da cimv2 raiz \\<br/>                                                 |
| MOF<br/>                      | <dl> <dt>Tscpub. mof</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>TscPubWmi.dll</dt> </dl> |



 

