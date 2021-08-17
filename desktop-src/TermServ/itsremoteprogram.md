---
title: Interface ITSRemoteProgram
description: Inclui métodos para definir e recuperar o modo RemoteApp e os parâmetros de inicialização para um programa RemoteApp, como o caminho do arquivo executável e o diretório de trabalho.
ms.assetid: c9eec63b-7162-4bf8-b5d5-8cadb971ef98
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de interface ITSRemoteProgram
- Serviços de Área de Trabalho Remota da interface ITSRemoteProgram, descrita
topic_type:
- apiref
api_name:
- ITSRemoteProgram
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b719771f265347da59ce4d8c5990a5b9dc5a72315780def0fd3a34b108e18169
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117756805"
---
# <a name="itsremoteprogram-interface"></a>Interface ITSRemoteProgram

Inclui métodos para definir e recuperar o modo RemoteApp e os parâmetros de inicialização para um programa RemoteApp, como o caminho do arquivo executável e o diretório de trabalho.

## <a name="members"></a>Membros

A interface **ITSRemoteProgram** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **ITSRemoteProgram** também tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A interface **ITSRemoteProgram** tem esses métodos.



| Método                                                            | Descrição                                                              |
|:------------------------------------------------------------------|:-------------------------------------------------------------------------|
| [**ServerStartProgram**](itsremoteprogram-serverstartprogram.md) | Especifica um programa do RemoteApp para iniciar na sessão remota.<br/> |



 

### <a name="properties"></a>Propriedades

A interface **ITSRemoteProgram** tem essas propriedades.



| Propriedade                                                                   | Tipo de acesso           | Descrição                    |
|:---------------------------------------------------------------------------|:----------------------|:-------------------------------|
| [**RemoteProgramMode**](itsremoteprogram-remoteprogrammode.md)<br/> | Leitura/gravação<br/> | O modo do RemoteApp.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ ITSRemoteProgram é definido como FDD029F9-467A-4c49-8529-64B521DBD1B4<br/>    |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[Referência de Conexão Web de Área de Trabalho Remota](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

