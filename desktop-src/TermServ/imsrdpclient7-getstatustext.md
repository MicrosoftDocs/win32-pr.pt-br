---
title: Método IMsRdpClient7 GetStatusText (OpenService. h)
description: Recupera o texto de status do código de status especificado.
ms.assetid: 1da2280a-c26d-4caa-b227-c289055f3aa9
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método GetStatusText
- Método GetStatusText Serviços de Área de Trabalho Remota, interface IMsRdpClient7
- Serviços de Área de Trabalho Remota de interface IMsRdpClient7, método GetStatusText
- Método GetStatusText Serviços de Área de Trabalho Remota, interface IMsRdpClient8
- Serviços de Área de Trabalho Remota de interface IMsRdpClient8, método GetStatusText
- Método GetStatusText Serviços de Área de Trabalho Remota, interface IMsRdpClient9
- Serviços de Área de Trabalho Remota de interface IMsRdpClient9, método GetStatusText
- Método GetStatusText Serviços de Área de Trabalho Remota, interface IMsRdpClient10
- Serviços de Área de Trabalho Remota de interface IMsRdpClient10, método GetStatusText
topic_type:
- apiref
api_name:
- IMsRdpClient7.GetStatusText
- IMsRdpClient8.GetStatusText
- IMsRdpClient9.GetStatusText
- IMsRdpClient10.GetStatusText
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 820628bfba59ec980e5128b9d9df3ee21b49a064
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644810"
---
# <a name="imsrdpclient7getstatustext-method"></a>Método IMsRdpClient7:: GetStatusText

Recupera o texto de status do código de status especificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetStatusText(
  [in]          UINT statusCode,
  [out, retval] BSTR *pBstrStatusText
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*StatusCode* \[ no\]
</dt> <dd>

Um **uint** que especifica o código de status para o qual recuperar o texto.

</dd> <dt>

*pBstrStatusText* \[ out, retval\]
</dt> <dd>

O endereço de um **BSTR** que recebe o texto de status.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7<br/>                                                                     |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2<br/>                                                        |
| parâmetro<br/>                   | <dl> <dt>OpenService. h</dt> </dl> |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| IID<br/>                      | IID \_ IMsRdpClient7 é definido como b2a5b5ce-3461-444A-91D4-add26d070638<br/>         |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**IMsRdpClient7**](imsrdpclient7.md)
</dt> <dt>

[**IMsRdpClient8**](imsrdpclient8.md)
</dt> <dt>

[**IMsRdpClient9**](imsrdpclient9.md)
</dt> <dt>

[**IMsRdpClient10**](imsrdpclient10.md)
</dt> </dl>

 

 





