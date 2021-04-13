---
title: Método getindexmode de IConfigAsfWriter
description: O método getindexmode recupera o modo de índice temporal atual.
ms.assetid: beb874ea-d0d5-4323-a817-47984911da4c
keywords:
- Método getindexmode formato de mídia do Windows
- Método getindexmode formato de mídia do Windows, interface IConfigAsfWriter
- IConfigAsfWriter interface formato Windows Media, método getindexmode
topic_type:
- apiref
api_name:
- IConfigAsfWriter.GetIndexMode
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bb701f591579d3113e79b0b9b74167ac8de3d75f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366269"
---
# <a name="iconfigasfwritergetindexmode-method"></a>Método IConfigAsfWriter:: getindexmode

O método **Getindexmode** recupera o modo de índice temporal atual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetIndexMode(
  [out] BOOL *pbIndexFile
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pbIndexFile* \[ fora\]
</dt> <dd>

Ponteiro para uma variável do tipo **bool** que recebe a configuração do modo de índice temporal. Um valor **true** indica que o gravador ASF do WM está configurado para gravar arquivos indexados de temporal.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se o método for bem sucedido, ele retornará S \_ OK. Se falhar, ele retornará um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Use esse método para determinar se o [gravador ASF do WM](wm-asf-writer-filter.md) está configurado atualmente para gravar arquivos ASF indexados de forma temporal. Para obter mais informações sobre arquivos indexados de forma temporal e estruturados em quadros, consulte os comentários para [**IConfigAsfWriter:: Setindexmode**](iconfigasfwriter-setindexmode.md).

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))
</dt> </dl>

 

 