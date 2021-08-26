---
description: Remove o buffer de origem especificado da coleção de buffers de origem gerenciados pelo objeto IMFMediaSourceExtension.
ms.assetid: 2f29cbac-4261-41ee-84c8-cb73686aeee5
title: Método IMFMediaSourceExtension::RemoveSourceBuffer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaSourceExtension.RemoveSourceBuffer
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 52c15882b57191169f033ab8a3b6c2f50f10f8e20b8f081c7bc70b7509b9a58b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013966"
---
# <a name="imfmediasourceextensionremovesourcebuffer-method"></a>Método IMFMediaSourceExtension::RemoveSourceBuffer

Remove o buffer de origem especificado da coleção de buffers de origem gerenciados pelo [**objeto IMFMediaSourceExtension.**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT RemoveSourceBuffer(
  [in] IMFSourceBuffer *pSourceBuffer
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pSourceBuffer* \[ Em\]
</dt> <dd>

O buffer a ser removido.

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

[**IMFMediaSourceExtension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension)
</dt> </dl>

 

 




