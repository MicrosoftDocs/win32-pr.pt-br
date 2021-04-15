---
description: Executa verificações de segurança no objeto ActiveX especificado e retorna o local onde o arquivo. cab correspondente foi baixado.
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
ms.openlocfilehash: 6d590f5e0e7ecd881a51844737f8efddf34d6727
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506136"
---
# <a name="ieaxiservicecallbackverifyfile-method"></a>Método IeAxiServiceCallback:: VERIFYFILE

O método **VERIFYFILE** executa verificações de segurança no objeto ActiveX especificado e retorna o local onde o arquivo. cab correspondente foi baixado.

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

A URL do objeto ActiveX a ser verificado.

</dd> <dt>

*bstrApprovedFileName* \[ fora\]
</dt> <dd>

O nome do arquivo em que o arquivo. cab associado ao objeto ActiveX foi baixado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se o método for bem sucedido, o método retornará S \_ OK.

Se o método falhar, ele retornará um valor **HRESULT** que indica o erro. Para obter uma lista de códigos de erro comuns, consulte [valores comuns de HRESULT](/windows/desktop/SecCrypto/common-hresult-values).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista Business, Windows Vista Enterprise, \[ somente aplicativos de área de trabalho do Windows Vista Ultimate\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                 |
| IID<br/>                      | IID \_ IeAxiServiceCallback é definido como 1823E7BA-EC36-447A-9B2E-B4912E15AFE7<br/>                   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IeAxiServiceCallback**](ieaxiservicecallback.md)
</dt> </dl>

 

