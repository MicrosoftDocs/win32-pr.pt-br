---
description: Fecha a sessão de chave de mídia e deve ser chamada antes que a sessão de chave seja liberada.
ms.assetid: 97c6b4bd-a973-4475-a325-0373af9b54b1
title: 'Método IMFMediaKeySession:: Close'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaKeySession.Close
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 16e6efbe27c411c38dca92d12e05fe9395c4946b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105784182"
---
# <a name="imfmediakeysessionclose-method"></a>Método IMFMediaKeySession:: Close

Fecha a sessão de chave de mídia e deve ser chamada antes que a sessão de chave seja liberada.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Close();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1 \[ apenas aplicativos de área de trabalho\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]<br/>                                      |
| INSERI<br/>                      | <dl> <dt>Mfmediaengine. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMFMediaKeySession**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeysession)
</dt> </dl>

 

 




