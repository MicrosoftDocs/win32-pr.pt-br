---
description: executa verificações de segurança no objeto de ActiveX especificado e retorna o local onde o arquivo de .cab correspondente foi baixado.
ms.assetid: ba8e4f9b-1569-43f9-b27c-a987044fff41
title: 'Método IeAxiServiceCallback:: VERIFYFILE'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiServiceCallback.VerifyFile
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3c8072680d42e214304cae1f0a6002b7a1fbc036fc075c5c6777dd7612733a0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119414706"
---
# <a name="ieaxiservicecallbackverifyfile-method"></a>Método IeAxiServiceCallback:: VERIFYFILE

o método **verifyfile** executa verificações de segurança no objeto de ActiveX especificado e retorna o local onde o arquivo de .cab correspondente foi baixado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT VerifyFile(
  [in]  BSTR bstrFileUrl,
  [out] BSTR *bstrApprovedFileName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrFileUrl* \[ no\]
</dt> <dd>

a URL do objeto de ActiveX a ser verificado.

</dd> <dt>

*bstrApprovedFileName* \[ fora\]
</dt> <dd>

o nome do arquivo em que o arquivo de .cab associado ao objeto ActiveX foi baixado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o método for bem sucedido, o método retornará S \_ OK.

Se o método falhar, ele retornará um valor **HRESULT** que indica o erro. Para obter uma lista de códigos de erro comuns, consulte [valores comuns de HRESULT](/windows/desktop/SecCrypto/common-hresult-values).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows vista Business, Windows vista Enterprise, \[ somente os aplicativos de área de trabalho do Windows vista Ultimate\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                 |
| IID<br/>                      | IID \_ IeAxiServiceCallback é definido como 1823E7BA-EC36-447A-9B2E-B4912E15AFE7<br/>                   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IeAxiServiceCallback**](ieaxiservicecallback.md)
</dt> </dl>

 

