---
description: Obtém o estado de erro associado à sessão de chave de mídia.
ms.assetid: 4693b7d5-59ee-472f-83fc-1ecbcc165dac
title: Método IMFMediaKeySession::GetError
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaKeySession.GetError
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 7698d059bd7d930037096208668de91292bca9e67b13743d353d3f682ec905a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119357756"
---
# <a name="imfmediakeysessiongeterror-method"></a>Método IMFMediaKeySession::GetError

Obtém o estado de erro associado à sessão de chave de mídia.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetError(
   USHORT *code,
   DWORD  *systemCode
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*code* 
</dt> <dd>

O código de erro.

</dd> <dt>

*systemCode* 
</dt> <dd>

Informações de erro específicas da plataforma.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8.1 somente aplicativos da área de trabalho\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Windows Server 2012 Somente \[ aplicativos da área de trabalho R2\]<br/>                                      |
| Idl<br/>                      | <dl> <dt>Mfmediaengine.idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMFMediaKeySession**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeysession)
</dt> </dl>

 

 




