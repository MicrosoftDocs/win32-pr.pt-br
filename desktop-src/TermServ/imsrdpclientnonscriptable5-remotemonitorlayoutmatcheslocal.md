---
title: Propriedade IMsRdpClientNonScriptable5 RemoteMonitorLayoutMatchesLocal
description: Especifica se o layout do monitor remoto é idêntico ao layout do monitor local.
ms.assetid: 8F3C6650-870C-417C-82FC-E145FC360012
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade RemoteMonitorLayoutMatchesLocal
- Propriedade RemoteMonitorLayoutMatchesLocal Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable5, Propriedade RemoteMonitorLayoutMatchesLocal
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable5.RemoteMonitorLayoutMatchesLocal
- IMsRdpClientNonScriptable5.get_RemoteMonitorLayoutMatchesLocal
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5018b22865cc683fc9231c857a1b99b8acbfeca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085869"
---
# <a name="imsrdpclientnonscriptable5remotemonitorlayoutmatcheslocal-property"></a>Propriedade IMsRdpClientNonScriptable5:: RemoteMonitorLayoutMatchesLocal

Especifica se o layout do monitor remoto é idêntico ao layout do monitor local. Se essa propriedade contiver a **variante \_ true**, o layout do monitor remoto será idêntico ao layout do monitor local. Se essa propriedade contiver a **variante \_ false**, os monitores remoto e local terão layouts diferentes.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_RemoteMonitorLayoutMatchesLocal(
  [out, retval] VARIANT_BOOL *pfRemoteMatchesLocal
);
```



## <a name="property-value"></a>Valor da propriedade

Recebe o valor da propriedade.

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

 

 





