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
ms.openlocfilehash: 92bf3d64d36c043e9e33b897294ff74a3fda0445
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105813304"
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

[**IMFMediaEngineClassFactoryEx**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineclassfactoryex)
</dt> </dl>

 

 




