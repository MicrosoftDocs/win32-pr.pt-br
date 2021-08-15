---
title: Categorizando por funcionalidades de contêiner
description: Os componentes geralmente exigem determinada funcionalidade do contêiner e não funcionarão com um contêiner que não oferece suporte.
ms.assetid: 11002f3e-17de-4e05-a2df-0c9e6326846d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67811a40c2c1bbffd4529b3f7c885a0d3e2bea19bda04035ffb80b601c266807
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118310883"
---
# <a name="categorizing-by-container-capabilities"></a>Categorizando por funcionalidades de contêiner

Os componentes geralmente exigem determinada funcionalidade do contêiner e não funcionarão com um contêiner que não oferece suporte. A interface do usuário deve filtrar componentes que exigem a funcionalidade que o contêiner não dá suporte. Para fazer isso, os componentes podem ser categorizados pela funcionalidade de contêiner necessária.

Um exemplo de componentes que exigem funcionalidade do contêiner e não funcionam em contêineres que não suportam essa funcionalidade são controles OLE de quadro simples. A categorização por funcionalidades de contêiner é realizada por uma chave adicional do Registro dentro da chave CLSID do componente:

``` syntax
;The CLSID for "Simple Frame Control" is {123456FF-ABCD-4321-0101-00000000000C}HKEY_CASSES_ROOT\CLSID\{12346FF-ABCD-4321-0101-00000000000C}\Implemented Categories
;The CATID for "Control" is {40FC6ED4-2438-11cf-A3DB-080036F12502} HKEY_CLASSES_ROOT\CLSID\{123456FF-ABCD-4321-0101-00000000000C}Implemented Categories\{40FC6ED4-2438-11cf-A3DB-080036F12502}
;The CATID for simple frame controls is {...CATID_SimpleFrameControl...} HKEY_CLASSES_ROOT\CLSID\{123456FF-ABCD-4321-0101-00000000000C}Implemented Categories\{...CATID_SimpleFrameControl...}
HKEY_CLASSES_ROOT\CLSID\{123456FF-ABCD-4321-0101-00000000000C}Required Categories\{...CATID_SimpleFrameControl...}
 
```

Conforme mostrado neste exemplo, um componente pode pertencer a categorias de componente que indicam a funcionalidade com suporte, bem como a categorias de componente que indicam a funcionalidade necessária.

No exemplo a seguir, o controle de botão é um controle OLE genérico que não dá suporte a nenhuma funcionalidade adicional. Ele funcionará em qualquer contêiner de controle OLE.

``` syntax
HKEY_CLASSES_ROOT\CLSID\{...CLSID_Button...}\Implemented Categories
HKEY_CLASSES_ROOT\CLSID\{...CLSID_Button...}\Implemented Categories\{...CATID_Control...}
 
```

Compare o exemplo anterior com o próximo exemplo no qual o MyDBControl poderá usar Visual Basic de dados se o contêiner for compatível com ele. No entanto, ele foi definido para que funcione em contêineres que não são Visual Basic associação de dados (talvez por uma API de banco de dados diferente):

``` syntax
HKEY_CLASSES_ROOT\CLSID\{...CLSID_MyDBControl...}\Implemented Categories
HKEY_CLASSES_ROOT\CLSID\{...CLSID_MyDBControl...}\Implemented Categories\{...CATID_Control...}
HKEY_CLASSES_ROOT\CLSID\{...CLSID_MyDBControl...}\Implemented Categories\{...CATID_VBDatabound...}
 
```

O controle GroupBox é um controle de quadro simples. Ele se baseia no contêiner que implementa a interface [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) e funcionará corretamente somente nesses contêineres:

``` syntax
HKEY_CLASSES_ROOT\CLSID\{...CLSID_GroupBox...}\Implemented Categories
HKEY_CLASSES_ROOT\CLSID\{...CLSID_GroupBox...}\Implemented Categories\{...CATID_Control...}
HKEY_CLASSES_ROOT\CLSID\{...CLSID_GroupBox...}\Implemented Categories\{...CATID_SimpleFrame...}
HKEY_CLASSES_ROOT\CLSID\{...CLSID_GroupBox...}\Required Categories\{...CATID_SimpleFrame...}
 
```

Um contêiner que dá suporte Visual Basic controles de limite de dados, mas não dá suporte a controles de quadro simples, especificaria o Controle CATID e \_ CATID VBDatabound para a interface do usuário do controle \_ de inserção. A lista de controles exibidos para o usuário conteria o botão CLSID \_ e o ClSID \_ MyDBControl. ClSID \_ GroupBox não seria exibido.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Associando ícones a uma categoria](associating-icons-with-a-category.md)
</dt> <dt>

[Categorizando por funcionalidades de componente](categorizing-by-component-capabilities.md)
</dt> <dt>

[Classes e associações padrão](default-classes-and-associations.md)
</dt> <dt>

[Definindo categorias de componentes](defining-component-categories.md)
</dt> <dt>

[O Gerenciador de Categorias de Componentes](the-component-categories-manager.md)
</dt> </dl>

 

 




