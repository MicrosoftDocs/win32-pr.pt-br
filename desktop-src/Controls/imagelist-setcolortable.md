---
title: Função ImageList_SetColorTable
description: Define a tabela de cores para uma lista de imagens.
ms.assetid: 1b62f468-cbc4-479b-b9f8-5553c2bd8c79
keywords:
- controles de Windows de função ImageList_SetColorTable
topic_type:
- apiref
api_name:
- ImageList_SetColorTable
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7de1acd8f14d9993bc75ea69b910b365e29156a6386933ccb95251a916c37244
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118412234"
---
# <a name="imagelist_setcolortable-function"></a>\_Função ImageList Setcolortable

Define a tabela de cores para uma lista de imagens.

## <a name="syntax"></a>Sintaxe


```C++
int ImageList_SetColorTable(
  _In_ HIMAGELIST himl,
  _In_ int        start,
  _In_ int        len,
  _In_ RGBQUAD    *prgb
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*himl* \[ no\]
</dt> <dd>

Tipo: **HIMAGELIST**

Um identificador para a lista de imagens.

</dd> <dt>

*Iniciar* \[ no\]
</dt> <dd>

Tipo: **int**

Um índice de tabela de cores com base em zero que especifica a primeira entrada da tabela de cores a ser definida.

</dd> <dt>

*Len* \[ no\]
</dt> <dd>

Tipo: **int**

O número de entradas da tabela de cores a serem definidas.

</dd> <dt>

*prgb* \[ no\]
</dt> <dd>

Tipo: **[ **RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad)\***

Um ponteiro para uma matriz de *Len* estruturas [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) contendo novas informações de cor para a tabela de cores do DIB.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **int**

Se a função for realizada com sucesso, ela retornará o número de entradas da tabela de cores definidas pela função. Se a função falhar, o valor de retorno será menor ou igual a zero.

## <a name="remarks"></a>Comentários

Somente as listas de imagens criadas com o sinalizador [**ILC \_ COLOR4**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) ou [**ILC \_ COLOR8**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) têm tabelas de cores. A tabela de cores dessa lista de imagens normalmente é definida automaticamente copiando a tabela de cores da primeira imagem adicionada à lista (por exemplo, por meio da função [**ImageList \_ Add**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_add) ) se essa imagem for uma DIB. Se a primeira imagem adicionada à lista de imagens não for uma DIB, a tabela de cores da paleta de retícula será usada para listas de imagens **ILC \_ COLOR8** e a tabela de cores VGA será usada para **ILC \_ COLOR4**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                                                  |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                                            |
| DLL<br/>                      | <dl> <dt>Comctl32.dll (versão 3,51 ou posterior)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Tabela de cores](https://msdn.microsoft.com/library/ms531197(v=VS.85).aspx)
</dt> </dl>

 

