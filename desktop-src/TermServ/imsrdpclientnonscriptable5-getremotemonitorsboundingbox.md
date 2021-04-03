---
title: Propriedade IMsRdpClientNonScriptable5 GetRemoteMonitorsBoundingBox
description: Especifica o retângulo delimitador do monitor remoto.
ms.assetid: 4A8794F7-1DB4-4415-8538-6B2A365B22D3
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade GetRemoteMonitorsBoundingBox
- Propriedade GetRemoteMonitorsBoundingBox Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable5, Propriedade GetRemoteMonitorsBoundingBox
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable5.GetRemoteMonitorsBoundingBox
- IMsRdpClientNonScriptable5.get_GetRemoteMonitorsBoundingBox
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97f67192b78c734359fc6113969eb5eb410e1bf3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918738"
---
# <a name="imsrdpclientnonscriptable5getremotemonitorsboundingbox-property"></a>Propriedade IMsRdpClientNonScriptable5:: GetRemoteMonitorsBoundingBox

Especifica o retângulo delimitador do monitor remoto.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_GetRemoteMonitorsBoundingBox(
  [out] LONG *pLeft,
  [out] LONG *pTop,
  [out] LONG *pRight,
  [out] LONG *pBottom
);
```



## <a name="property-value"></a>Valor da propriedade

Recebe a borda esquerda do retângulo.

Recebe a borda superior do retângulo.

Recebe a borda direita do retângulo.

Recebe a borda inferior do retângulo.

## <a name="remarks"></a>Comentários

Todas as coordenadas estão em coordenadas de tela virtual, que são relativas ao canto superior esquerdo do monitor primário. Se esse não for o monitor primário, alguns ou todos esses valores poderão ser negativos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7<br/>                                                                          |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2<br/>                                                             |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| IID<br/>                      | IID \_ IMsRdpClientNonScriptable5 é definido como 4f6996d5-d7b1-412C-b0ff-063718566907<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> </dl>

 

 





