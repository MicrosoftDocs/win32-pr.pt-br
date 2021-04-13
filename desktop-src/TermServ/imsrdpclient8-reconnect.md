---
title: Método de reconexão do IMsRdpClient8
description: Reconecta-se à sessão remota com a nova largura e altura da área de trabalho.
ms.assetid: A2C4101D-780A-4973-B87C-025D9140C4BC
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método de reconexão
- Método reconnect Serviços de Área de Trabalho Remota, interface IMsRdpClient8
- Serviços de Área de Trabalho Remota de interface IMsRdpClient8, método reconnect
- Método reconnect Serviços de Área de Trabalho Remota, interface IMsRdpClient9
- Serviços de Área de Trabalho Remota de interface IMsRdpClient9, método reconnect
- Método reconnect Serviços de Área de Trabalho Remota, interface IMsRdpClient10
- Serviços de Área de Trabalho Remota de interface IMsRdpClient10, método reconnect
topic_type:
- apiref
api_name:
- IMsRdpClient8.Reconnect
- IMsRdpClient9.Reconnect
- IMsRdpClient10.Reconnect
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d62072c56852af6be2965ce63aecf4634de87d11
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499848"
---
# <a name="imsrdpclient8reconnect-method"></a>Método IMsRdpClient8:: Reconnect

Reconecta-se à sessão remota com a nova largura e altura da área de trabalho. O controle já deve estar conectado a uma sessão remota para que esse método tenha sucesso.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Reconnect(
  [in]          ULONG                  ulWidth,
  [in]          ULONG                  ulHeight,
  [out, retval] ControlReconnectStatus *pReconnectStatus
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ulWidth* \[ no\]
</dt> <dd>

Tipo: **ULONG**

A nova largura da área de trabalho, em pixels. Consulte a propriedade [**DesktopWidth**](imstscax-desktopwidth.md) para restrições de valor.

</dd> <dt>

*ulHeight* \[ no\]
</dt> <dd>

Tipo: **ULONG**

A nova altura da área de trabalho, em pixels. Consulte a propriedade [**DesktopHeight**](imstscax-desktopheight.md) para restrições de valor.

</dd> <dt>

*pReconnectStatus* \[ out, retval\]
</dt> <dd>

Tipo: **[**ControlReconnectStatus**](controlreconnectstatus.md) \** _

Um ponteiro para uma variável [_ *ControlReconnectStatus* *](controlreconnectstatus.md) que recebe o status da operação de reconexão.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8<br/>                                                                   |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpClient8 é definido como 4247E044-9271-43A9-BC49-E2AD9E855D62<br/>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsRdpClient8**](imsrdpclient8.md)
</dt> <dt>

[**IMsRdpClient9**](imsrdpclient9.md)
</dt> <dt>

[**IMsRdpClient10**](imsrdpclient10.md)
</dt> <dt>

[**ControlReconnectStatus**](controlreconnectstatus.md)
</dt> </dl>

 

 





