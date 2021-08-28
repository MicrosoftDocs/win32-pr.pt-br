---
title: Propriedade ITSRemoteProgram RemoteProgramMode
description: o modo do RemoteApp do Windows Server 2008 R2.
ms.assetid: 9ebdf966-db9c-4a14-8469-f8b153c6ea78
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade RemoteProgramMode
- Propriedade RemoteProgramMode Serviços de Área de Trabalho Remota, interface ITSRemoteProgram
- Serviços de Área de Trabalho Remota de interface ITSRemoteProgram, Propriedade RemoteProgramMode
- Propriedade RemoteProgramMode Serviços de Área de Trabalho Remota, interface ITSRemoteProgram2
- Serviços de Área de Trabalho Remota de interface ITSRemoteProgram2, Propriedade RemoteProgramMode
- Propriedade RemoteProgramMode Serviços de Área de Trabalho Remota, interface ITSRemoteProgram3
- Serviços de Área de Trabalho Remota de interface ITSRemoteProgram3, Propriedade RemoteProgramMode
topic_type:
- apiref
api_name:
- ITSRemoteProgram.RemoteProgramMode
- ITSRemoteProgram.get_RemoteProgramMode
- ITSRemoteProgram.put_RemoteProgramMode
- ITSRemoteProgram2.RemoteProgramMode
- ITSRemoteProgram2.get_RemoteProgramMode
- ITSRemoteProgram2.put_RemoteProgramMode
- ITSRemoteProgram3.RemoteProgramMode
- ITSRemoteProgram3.get_RemoteProgramMode
- ITSRemoteProgram3.put_RemoteProgramMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c36f450e6cbfec3922a56a42bc2f1f61466774eeff46c0987b6fad4ca9dc9731
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124816"
---
# <a name="itsremoteprogramremoteprogrammode-property"></a>Propriedade ITSRemoteProgram:: RemoteProgramMode

o modo do RemoteApp do Windows Server 2008 R2.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_RemoteProgramMode(
  [in]  VARIANT_BOOL vboolRemoteProgramMode
);

HRESULT get_RemoteProgramMode(
  [out] VARIANT_BOOL *pvboolRemoteProgramMode
);
```



## <a name="property-value"></a>Valor da propriedade

O modo do RemoteApp. Se definido como **Variant \_ true**, o modo RemoteApp será habilitado e a sessão remota hospedará os programas do RemoteApp. Se definido como **Variant \_ false** (o padrão), o modo RemoteApp não está habilitado. A sessão remota irá hospedar uma área de trabalho remota.

## <a name="error-codes"></a>Códigos do Erro

Retornará **S \_ OK** se for bem-sucedido.

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

[**ITSRemoteProgram2**](itsremoteprogram2.md)
</dt> <dt>

[**ITSRemoteProgram3**](itsremoteprogram3.md)
</dt> <dt>

[**ITSRemoteProgram**](itsremoteprogram.md)
</dt> </dl>

 

 





