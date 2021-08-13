---
title: Método GetStatusText IMsRdpClient7 (Openservice.h)
description: Recupera o texto de status para o código de status especificado.
ms.assetid: 1da2280a-c26d-4caa-b227-c289055f3aa9
ms.tgt_platform: multiple
keywords:
- Método GetStatusText Serviços de Área de Trabalho Remota
- Método GetStatusText Serviços de Área de Trabalho Remota interface , IMsRdpClient7
- Interface IMsRdpClient7 Serviços de Área de Trabalho Remota , método GetStatusText
- Método GetStatusText Serviços de Área de Trabalho Remota interface , IMsRdpClient8
- Interface IMsRdpClient8 Serviços de Área de Trabalho Remota , método GetStatusText
- Método GetStatusText Serviços de Área de Trabalho Remota interface , IMsRdpClient9
- Interface IMsRdpClient9 Serviços de Área de Trabalho Remota , método GetStatusText
- Método GetStatusText Serviços de Área de Trabalho Remota interface , IMsRdpClient10
- Interface IMsRdpClient10 Serviços de Área de Trabalho Remota , método GetStatusText
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
ms.openlocfilehash: 42ecccb6535afec2d32ff0466428af36c432bc981a1bc23cfa24161ca969a80e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119285186"
---
# <a name="imsrdpclient7getstatustext-method"></a>Método IMsRdpClient7::GetStatusText

Recupera o texto de status para o código de status especificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetStatusText(
  [in]          UINT statusCode,
  [out, retval] BSTR *pBstrStatusText
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*statusCode* \[ Em\]
</dt> <dd>

Um **UINT** que especifica o código de status para o que recuperar o texto.

</dd> <dt>

*pBstrStatusText* \[ out, retval\]
</dt> <dd>

O endereço de um **BSTR** que recebe o texto de status.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7<br/>                                                                     |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2<br/>                                                        |
| parâmetro<br/>                   | <dl> <dt>Openservice.h</dt> </dl> |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| IID<br/>                      | IID \_ IMsRdpClient7 é definido como b2a5b5ce-3461-444a-91d4-add26d070638<br/>         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsRdpClient7**](imsrdpclient7.md)
</dt> <dt>

[**IMsRdpClient8**](imsrdpclient8.md)
</dt> <dt>

[**IMsRdpClient9**](imsrdpclient9.md)
</dt> <dt>

[**IMsRdpClient10**](imsrdpclient10.md)
</dt> </dl>

 

 





