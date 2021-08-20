---
description: Obtém um valor que indica se o sistema de chave especificado dá suporte ao tipo de mídia especificado.
ms.assetid: 6f4f50db-e491-46c2-a8b2-1b8e51033b5b
title: 'Método IMFMediaEngineClassFactoryEx:: IsTypeSupported'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaEngineClassFactoryEx.IsTypeSupported
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 588a7fdc02fb59a9dc156f9f141b210d36e4cef131bf353d6c98d9c055392a28
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118062995"
---
# <a name="imfmediaengineclassfactoryexistypesupported-method"></a>Método IMFMediaEngineClassFactoryEx:: IsTypeSupported

Obtém um valor que indica se o sistema de chave especificado dá suporte ao tipo de mídia especificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IsTypeSupported(
   BSTR type,
   BSTR keySystem,
   BOOL *isSupported
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*tipo* 
</dt> <dd>

O tipo de MIME para o qual verificar o suporte.

</dd> <dt>

*sistema de* 
</dt> <dd>

O sistema principal para o qual verificar o suporte.

</dd> <dt>

*isSupported* 
</dt> <dd>

**true** se o tipo for compatível com o *keysystem*; caso contrário, **false.**

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

[**IMFMediaEngineClassFactoryEx**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineclassfactoryex)
</dt> </dl>

 

 




