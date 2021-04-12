---
title: Classes e associações padrão
description: Para determinadas categorias, uma única classe pode ser associada como a classe padrão.
ms.assetid: 9c48615b-ab10-44e4-a032-49d5ee0c9b01
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 871c537535c57da0809effbe3ee8ec086a88fd5c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363672"
---
# <a name="default-classes-and-associations"></a>Classes e associações padrão

Para determinadas categorias, uma única classe pode ser associada como a classe padrão. A classe padrão é selecionada sempre que essa categoria de objeto em particular é necessária. Embora isso possa não ser útil para todas as categorias de componente, o estabelecimento de uma classe padrão pode ser útil quando uma determinada classe deve ser carregada de uma lista de classes possíveis sem intervenção do usuário. Os administradores definem qual classe pode ser usada manipulando o registro.

Para associar uma classe padrão a uma categoria, introduza uma chave CLSID com o mesmo CLSID que o CATID da categoria de componente escolhida como padrão. Em seguida, adicione uma chave Treats a essa chave, usando o valor para o CLSID da classe padrão para a categoria. Para usar a classe padrão para uma categoria de componente, use [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) ou [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject), especificando o CATID para o parâmetro CLSID. Isso redireciona automaticamente para o CLSID estabelecido como o padrão para essa categoria. A entrada do registro é a seguinte:

```
HKEY_CLASSES_ROOT\CLSID
   {catid}
      TreatAs
          = default clsid
```

Durante a instalação, um componente pode verificar a existência de qualquer chave de classe padrão para suas categorias e apresentar ao usuário opções para substituir as configurações atuais.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Associando ícones a uma categoria](associating-icons-with-a-category.md)
</dt> <dt>

[Categorizando por recursos de componente](categorizing-by-component-capabilities.md)
</dt> <dt>

[Categorizando por recursos de contêiner](categorizing-by-container-capabilities.md)
</dt> <dt>

[Definindo categorias de componentes](defining-component-categories.md)
</dt> <dt>

[O Gerenciador de categorias de componentes](the-component-categories-manager.md)
</dt> </dl>

 

 




