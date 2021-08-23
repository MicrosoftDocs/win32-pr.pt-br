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
ms.openlocfilehash: 2dd9bcc7a1151b042d275917e8bd8106eb079de3315137ca41fa7faecaf5c957
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119942036"
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

*Tipo MIME* 
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

## <a name="return-value"></a>Valor retornado

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1 \[ somente aplicativos da área de trabalho\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[Somente aplicativos da área de trabalho R2\]<br/>                                      |
| INSERI<br/>                      | <dl> <dt>Mfmediaengine. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMFMediaKeys**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeys)
</dt> </dl>

 

 




