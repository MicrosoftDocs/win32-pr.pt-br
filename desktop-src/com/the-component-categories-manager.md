---
title: O Gerenciador de categorias de componentes
description: O Gerenciador de categorias de componentes
ms.assetid: bd43ef98-2299-4c8a-9f35-bf9aceb074ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fdf301e1b344bbc2403fd656dd90447ccffc357
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453590"
---
# <a name="the-component-categories-manager"></a>O Gerenciador de categorias de componentes

Para facilitar o manuseio de categorias de componentes e garantir a consistência do registro, o sistema fornece o Gerenciador de categorias de componentes, um objeto COM com um CLSID de CLSID \_ StdComponentCategoriesMgr. Este objeto COM fornece as seguintes interfaces:

-   [**ICatInformation**](/windows/desktop/api/ComCat/nn-comcat-icatinformation)
-   [**ICatRegister**](/windows/desktop/api/ComCat/nn-comcat-icatregister)

O [**ICatInformation**](/windows/desktop/api/ComCat/nn-comcat-icatinformation) fornece métodos para obter informações sobre as categorias implementadas ou exigidas por uma determinada classe e fornece informações sobre as categorias registradas em determinado computador.

O [**ICatRegister**](/windows/desktop/api/ComCat/nn-comcat-icatregister) fornece métodos para registrar e cancelar o registro de informações de categoria de componente no registro. Isso inclui os nomes legíveis de categorias e as categorias implementadas ou exigidas por um determinado componente ou classe.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Associando ícones a uma categoria](associating-icons-with-a-category.md)
</dt> <dt>

[Categorizando por recursos de componente](categorizing-by-component-capabilities.md)
</dt> <dt>

[Categorizando por recursos de contêiner](categorizing-by-container-capabilities.md)
</dt> <dt>

[Classes e associações padrão](default-classes-and-associations.md)
</dt> <dt>

[Definindo categorias de componentes](defining-component-categories.md)
</dt> </dl>

 

 




