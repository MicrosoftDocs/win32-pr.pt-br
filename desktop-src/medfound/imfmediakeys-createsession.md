---
description: Cria um objeto de sessão de chave de mídia usando os dados de inicialização especificados e os dados personalizados. .
ms.assetid: 9f11433c-7cff-4a59-9d4a-7f4b56ba62cf
title: 'Método IMFMediaKeys:: CreateSession'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaKeys.CreateSession
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 89d3abce0c1c15d472f7008fa0ef2c5f27bba6ad
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105813481"
---
# <a name="imfmediakeyscreatesession-method"></a>Método IMFMediaKeys:: CreateSession

Cria um objeto de sessão de chave de mídia usando os dados de inicialização especificados e os dados personalizados. .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CreateSession(
         BSTR                     mimeType,
   const BYTE                     *initData,
         DWORD                    cb,
   const BYTE                     *customData,
         DWORD                    cbCustomData,
         IMFMediaKeySessionNotify *notify,
         IMFMediaKeySession       **ppSession
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*MIME* 
</dt> <dd>

O tipo MIME do contêiner de mídia usado para o conteúdo.

</dd> <dt>

*initData* 
</dt> <dd>

Os dados de inicialização para o sistema de chaves.

</dd> <dt>

*CB* 
</dt> <dd>

A contagem em bytes de *initdata*.

</dd> <dt>

*customData* 
</dt> <dd>

Dados personalizados enviados para o sistema de chaves.

</dd> <dt>

*cbCustomData* 
</dt> <dd>

A contagem em bytes de *cbCustomData*.

</dd> <dt>

*sobre* 
</dt> <dd>

sobre

</dd> <dt>

*ppSession* 
</dt> <dd>

A sessão de chave de mídia.

</dd> </dl>

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

[**IMFMediaKeys**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeys)
</dt> </dl>

 

 




