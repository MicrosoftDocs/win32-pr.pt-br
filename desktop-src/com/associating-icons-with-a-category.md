---
title: Associando ícones a uma categoria
description: Associando ícones a uma categoria
ms.assetid: 5e5c3c10-07cf-4a34-9822-97ec940b3117
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62af14480d24053ffc517d405635ecbe4d6e45c8edac256039ea008160f11063
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793826"
---
# <a name="associating-icons-with-a-category"></a>Associando ícones a uma categoria

A criação de uma interface do usuário que permite ao usuário selecionar categorias de componentes em uma categoria requer a capacidade de exibir uma imagem significativa para uma determinada categoria. Para associar um ícone a uma categoria de componente, crie uma chave para o CATID da categoria e preencha essa chave com uma subchave [DefaultIcon](defaulticon.md) . A entrada do registro é a seguinte:

``` syntax
HKEY_CLASSES_ROOT\CLSID\{...catid...}\DefaultIcon = "c:\hello\icons.dll,1"
 
```

O nome de arquivo referenciado pela chave DefaultIcon pode ser um executável ou um arquivos DLL (DLL somente de recursos).

Para associar um pequeno "bitmap de caixa de ferramentas" 16x16 a uma categoria de componente, crie uma chave em **\_ classe HKEY \_ raiz \\ CLSID** para o CATID da categoria e preencha essa chave com uma subchave [ToolBoxBitmap32](toolboxbitmap32.md) , conforme mostrado no exemplo a seguir:

``` syntax
HKEY_CLASSES_ROOT\CLSID\{...catid...}\ToolBoxBitmap32 = "c:\goodbye\mycomponent.dll,42"
 
```

O nome de arquivo referenciado pela chave [ToolBoxBitmap32](toolboxbitmap32.md) também pode ser um arquivos exe ou DLL (DLL somente de recursos).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Categorizando por recursos de componente](categorizing-by-component-capabilities.md)
</dt> <dt>

[Categorizando por recursos de contêiner](categorizing-by-container-capabilities.md)
</dt> <dt>

[Classes e associações padrão](default-classes-and-associations.md)
</dt> <dt>

[Definindo categorias de componentes](defining-component-categories.md)
</dt> <dt>

[**ICatInformation**](/windows/desktop/api/ComCat/nn-comcat-icatinformation)
</dt> <dt>

[**ICatRegister**](/windows/desktop/api/ComCat/nn-comcat-icatregister)
</dt> <dt>

[O Gerenciador de categorias de componentes](the-component-categories-manager.md)
</dt> </dl>

 

 




