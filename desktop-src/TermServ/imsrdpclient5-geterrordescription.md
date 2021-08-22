---
title: Método IMsRdpClient5 GetErrorDescription
description: Recupera a descrição do erro para os eventos de desconexão de sessão.
ms.assetid: 8c8f7b10-7f79-4586-845e-e99f5ca81905
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método GetErrorDescription
- Método GetErrorDescription Serviços de Área de Trabalho Remota, interface IMsRdpClient5
- Serviços de Área de Trabalho Remota de interface IMsRdpClient5, método GetErrorDescription
- Método GetErrorDescription Serviços de Área de Trabalho Remota, interface IMsRdpClient6
- Serviços de Área de Trabalho Remota de interface IMsRdpClient6, método GetErrorDescription
- Método GetErrorDescription Serviços de Área de Trabalho Remota, interface IMsRdpClient7
- Serviços de Área de Trabalho Remota de interface IMsRdpClient7, método GetErrorDescription
- Método GetErrorDescription Serviços de Área de Trabalho Remota, interface IMsRdpClient8
- Serviços de Área de Trabalho Remota de interface IMsRdpClient8, método GetErrorDescription
- Método GetErrorDescription Serviços de Área de Trabalho Remota, interface IMsRdpClient9
- Serviços de Área de Trabalho Remota de interface IMsRdpClient9, método GetErrorDescription
- Método GetErrorDescription Serviços de Área de Trabalho Remota, interface IMsRdpClient10
- Serviços de Área de Trabalho Remota de interface IMsRdpClient10, método GetErrorDescription
topic_type:
- apiref
api_name:
- IMsRdpClient5.GetErrorDescription
- IMsRdpClient6.GetErrorDescription
- IMsRdpClient7.GetErrorDescription
- IMsRdpClient8.GetErrorDescription
- IMsRdpClient9.GetErrorDescription
- IMsRdpClient10.GetErrorDescription
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 197025b4cfb842cf4ca38af64124c02415240ac6fc878f9c121d4e228b77f5b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001484"
---
# <a name="imsrdpclient5geterrordescription-method"></a>Método IMsRdpClient5:: GetErrorDescription

Recupera a descrição do erro para os eventos de desconexão de sessão.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetErrorDescription(
  [in]  UINT disconnectReason,
  [in]  UINT extendedDisconnectReason,
  [out] BSTR *pBstrErrorMsg
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*disconnectReason* \[ no\]
</dt> <dd>

O motivo da desconexão.

</dd> <dt>

*extendedDisconnectReason* \[ no\]
</dt> <dd>

Fornece informações detalhadas sobre por que uma desconexão foi iniciada.

</dd> <dt>

*pBstrErrorMsg* \[ fora\]
</dt> <dd>

Um ponteiro para uma variável **BSTR** que recebe o texto da mensagem de erro.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpClient5 é definido como 4eb5335b-6429-477d-b922-e06a28ecd8bf<br/>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsRdpClient5**](imsrdpclient5.md)
</dt> <dt>

[**IMsRdpClient6**](imsrdpclient6.md)
</dt> <dt>

[**IMsRdpClient7**](imsrdpclient7.md)
</dt> <dt>

[**IMsRdpClient8**](imsrdpclient8.md)
</dt> <dt>

[**IMsRdpClient9**](imsrdpclient9.md)
</dt> <dt>

[**IMsRdpClient10**](imsrdpclient10.md)
</dt> </dl>

 

 





