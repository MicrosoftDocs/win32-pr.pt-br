---
description: Obtém as informações de tipo de um item.
ms.assetid: 9670f184-e8ba-4596-af6d-2967320dfd95
title: 'Método IWiaItem2:: GetItemType (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.GetItemType
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 3bf177ddcc117cdfe21a1b9322a0e457cf899c0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647220"
---
# <a name="iwiaitem2getitemtype-method"></a>Método IWiaItem2:: GetItemType

Obtém as informações de tipo de um item.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetItemType(
  [out] LONG *pItemType
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pItemType* \[ fora\]
</dt> <dd>

Tipo: **Long \** _

Recebe um ponteiro para um _ *Long** que contém uma combinação de sinalizadores de tipo. Consulte [**sinalizadores de tipo de item WIA**](-wia-wia-item-type-flags.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Cada objeto [**IWiaItem2**](-wia-iwiaitem2.md) na árvore hierárquica de objetos associados a um dispositivo de hardware de aquisição de imagem do Windows (WIA) 2,0 tem um tipo de dados específico. Os objetos de item representam pastas e arquivos. As pastas contêm objetos de arquivo. Os objetos de arquivo contêm dados adquiridos pelo dispositivo, como imagens e sons. Esse método permite que os aplicativos identifiquem o tipo de qualquer item em uma árvore hierárquica de objetos de item em um dispositivo.

Um item pode ter mais de um tipo. Por exemplo, um item que representa um arquivo de áudio terá os atributos de tipo [**WiaItemTypeAudio**](-wia-wia-item-type-flags.md) \| **WiaItemTypeFile**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 




