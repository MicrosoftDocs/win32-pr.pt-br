---
description: Obtém um valor que indica se o tipo MIME especificado tem suporte da origem de mídia.
ms.assetid: 894ef7d2-d008-42e1-8a61-26f35a8877be
title: 'Método IMFMediaSourceExtension:: IsTypeSupported'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaSourceExtension.IsTypeSupported
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: e2292ab717914e29a7741fed997b0f8b8b16e152e2fa889dd7ecb04bbb98aaea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974335"
---
# <a name="imfmediasourceextensionistypesupported-method"></a>Método IMFMediaSourceExtension:: IsTypeSupported

Obtém um valor que indica se o tipo MIME especificado tem suporte da origem de mídia.

## <a name="syntax"></a>Sintaxe


```C++
BOOL IsTypeSupported(
  [in] BSTR type
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*tipo* \[ de no\]
</dt> <dd>

O tipo de mídia para o qual verificar o suporte.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

**true** se o tipo de mídia tiver suporte; caso contrário, **false**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1 \[ somente aplicativos da área de trabalho\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[Somente aplicativos da área de trabalho R2\]<br/>                                      |
| INSERI<br/>                      | <dl> <dt>Mfmediaengine. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMFMediaSourceExtension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension)
</dt> </dl>

 

 




