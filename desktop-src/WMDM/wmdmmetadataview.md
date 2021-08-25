---
title: Estrutura WMDMMetadataView
description: A estrutura WMDMMetadataView define a exibição de metadados. O conteúdo é organizado com base nessa definição.
ms.assetid: 787d2295-d433-451d-a1fc-6f73585e10d6
keywords:
- Estrutura WMDMMetadataView Windows Media Gerenciador de Dispositivos
topic_type:
- apiref
api_name:
- WMDMMetadataView
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e442ed3058f1982ac7607c6b8a29e5df321d69776695821b278049e27cd7589
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119862586"
---
# <a name="wmdmmetadataview-structure"></a>Estrutura WMDMMetadataView

A estrutura **WMDMMetadataView** define a exibição de metadados. O conteúdo é organizado com base nessa definição.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _WMDMMetadataView {
  WCHAR *pwszViewName;
  UINT  nDepth;
  WCHAR **ppwszTags;
} WMDMMetadataView;
```



## <a name="members"></a>Membros

<dl> <dt>

**pwszViewName**
</dt> <dd>

Ponteiro para uma cadeia de caracteres com terminação nula de caractere largo que contém o nome da exibição. Isso é usado como o nome do nó raiz no qual essa exibição é apresentada.

</dd> <dt>

**nDepth**
</dt> <dd>

Inteiro que contém a profundidade da exibição, que indica quantas marcas de metadados aninhadas são usadas para a exibição.

</dd> <dt>

**ppwszTags**
</dt> <dd>

Matriz de cadeias de caracteres de marca de metadados para as marcas aninhadas.

</dd> </dl>

## <a name="examples"></a>Exemplos

O código a seguir cria uma exibição de metadados:


```C++
WMDMMetadataView view;
view.pwszName = L"My View";
view.nDepth = 3;  // genre, artist, album
LPCWSTR wszTagArray[3]; 
wszTagArray[0] = g_wszWMDMGenre;
wszTagArray[1] = g_wszWMDMAuthor;
wszTagArray[2] = g_wszWMDMAlbumTitle;
view.ppwszTags = wszTagArray;
```



O código anterior organiza o conteúdo da seguinte maneira:

<dl> Minha exibição<dl> Genre1<dl> Artist1<dl> Album1<dl> Song1  
Song2  
...  
</dl> </dd> Album2  
...  
</dl> </dd> Artist2<dl> Album1<dl> Song1  
Song2  
...  
</dl> </dd> Album2  
...  
</dl> </dd> </dl> </dd> Genre2<dl> Artist1<dl> Album1<dl> Song1  
Song2  
...  
</dl> </dd> Album2  
...  
</dl> </dd> Artist2<dl> Album1<dl> Song1  
Song2  
...  
</dl> </dd> Album2  
...  
</dl> </dd> ...  
</dl> </dd> ...  
</dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>WMDM. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Estruturas**](structures.md)
</dt> </dl>

 

 





