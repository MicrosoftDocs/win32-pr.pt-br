---
title: Verbo
description: Especifica os verbos a serem registrados para um aplicativo.
ms.assetid: bfcad36d-a52a-4117-bf0b-6135b197a7ee
keywords:
- Chave do registro de verbo COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ef025ee0807ca3e75577f26f81951db22dfb0ac
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "105787723"
---
# <a name="verb"></a>Verbo

Especifica os verbos a serem registrados para um aplicativo.

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      Verb
         1 = verb1
         2 = verb2
         3 = ...
```

## <a name="remarks"></a>Comentários

Cada verbo é um valor " **\_ reg** " do formato "*nome*, *\_ sinalizador de menu*, *\_ sinalizador de verbo*". Os verbos devem ser numerados consecutivamente.

O *nome* descreve como o verbo é acrescentado por uma chamada de função [**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua) . Por exemplo, "&Play".

O valor do *\_ sinalizador de menu* indica como o verbo deve aparecer no menu. Todos os sinalizadores com suporte do [**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua) têm suporte, com exceção do \_ bitmap MF, MF \_ OWNERDRAW e \_ pop-up MF.

O valor do *\_ sinalizador de verbo* descreve os atributos dos verbos. Use um dos valores de [**OLEVERBATTRIB**](/windows/win32/api/oleidl/ne-oleidl-oleverbattrib)ou 0.

Para obter mais informações, consulte [**OLEVERB**](/windows/win32/api/oleidl/ns-oleidl-oleverb), [**IOleObject::D overb**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-doverb)e [**IOleObject:: EnumVerbs**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-enumverbs).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua)
</dt> <dt>

[**OLEVERB**](/windows/win32/api/oleidl/ns-oleidl-oleverb)
</dt> <dt>

[**OLEVERBATTRIB**](/windows/win32/api/oleidl/ne-oleidl-oleverbattrib)
</dt> </dl>

 

 