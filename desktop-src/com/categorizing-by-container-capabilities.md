---
title: Categorizando por recursos de contêiner
description: Os componentes geralmente exigem determinada funcionalidade do contêiner e não funcionarão com um contêiner que não forneça o suporte.
ms.assetid: 11002f3e-17de-4e05-a2df-0c9e6326846d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 987546c20ff77a40666bb74689466a15fab989a6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006086"
---
# <a name="categorizing-by-container-capabilities"></a>Categorizando por recursos de contêiner

Os componentes geralmente exigem determinada funcionalidade do contêiner e não funcionarão com um contêiner que não forneça o suporte. A interface do usuário deve filtrar os componentes que exigem a funcionalidade para a qual o contêiner não dá suporte. Para fazer isso, os componentes podem ser categorizados pela funcionalidade de contêiner necessária.

Um exemplo de componentes que exigem funcionalidade do contêiner e não funcionam em contêineres que não dão suporte a essa funcionalidade são controles OLE de quadro simples. A categorização por recursos de contêiner é realizada por uma chave de registro adicional na chave CLSID do componente:

``` syntax
;The CLSID for "Simple Frame Control" is {123456FF-ABCD-4321-0101-00000000000C}HKEY_CASSES_ROOT\CLSID\{12346FF-ABCD-4321-0101-00000000000C}\Implemented Categories
;The CATID for "Control" is {40FC6ED4-2438-11cf-A3DB-080036F12502} HKEY_CLASSES_ROOT\CLSID\{123456FF-ABCD-4321-0101-00000000000C}Implemented Categories\{40FC6ED4-2438-11cf-A3DB-080036F12502}
;The CATID for simple frame controls is {...CATID_SimpleFrameControl...} HKEY_CLASSES_ROOT\CLSID\{123456FF-ABCD-4321-0101-00000000000C}Implemented Categories\{...CATID_SimpleFrameControl...}
HKEY_CLASSES_ROOT\CLSID\{123456FF-ABCD-4321-0101-00000000000C}Required Categories\{...CATID_SimpleFrameControl...}
 
```

Como mostrado neste exemplo, um componente pode pertencer a categorias de componentes que indicam a funcionalidade com suporte, bem como categorias de componentes que indicam a funcionalidade necessária.

No exemplo a seguir, o controle Button é um controle OLE genérico que não dá suporte a nenhuma funcionalidade adicional. Ele funcionará em qualquer contêiner de controle OLE.

``` syntax
HKEY_CLASSES_ROOT\CLSID\{...CLSID_Button...}\Implemented Categories
HKEY_CLASSES_ROOT\CLSID\{...CLSID_Button...}\Implemented Categories\{...CATID_Control...}
 
```

Compare o exemplo anterior com o próximo exemplo no qual o MyDBControl pode usar Visual Basic vinculação de dados se o contêiner oferecer suporte a ele. No entanto, ele foi definido para que funcione em contêineres que não suportam Visual Basic Associação de dados (talvez por uma API de banco de dado diferente):

``` syntax
HKEY_CLASSES_ROOT\CLSID\{...CLSID_MyDBControl...}\Implemented Categories
HKEY_CLASSES_ROOT\CLSID\{...CLSID_MyDBControl...}\Implemented Categories\{...CATID_Control...}
HKEY_CLASSES_ROOT\CLSID\{...CLSID_MyDBControl...}\Implemented Categories\{...CATID_VBDatabound...}
 
```

O controle GroupBox é um controle Frame simples. Ele se baseia no contêiner que implementa a interface [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) e funcionará corretamente apenas nesses contêineres:

``` syntax
HKEY_CLASSES_ROOT\CLSID\{...CLSID_GroupBox...}\Implemented Categories
HKEY_CLASSES_ROOT\CLSID\{...CLSID_GroupBox...}\Implemented Categories\{...CATID_Control...}
HKEY_CLASSES_ROOT\CLSID\{...CLSID_GroupBox...}\Implemented Categories\{...CATID_SimpleFrame...}
HKEY_CLASSES_ROOT\CLSID\{...CLSID_GroupBox...}\Required Categories\{...CATID_SimpleFrame...}
 
```

Um contêiner que dá suporte a Visual Basic controles associados a dados, mas não dá suporte a controles de quadro simples especificaria \_ o controle CATID e \_ o CATID VBDatabound para a interface do usuário do controle de inserção. A lista de controles exibida para o usuário contém o botão CLSID \_ e CLSID \_ MyDBControl. A caixa de caixa do CLSID \_ não seria exibida.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Associando ícones a uma categoria](associating-icons-with-a-category.md)
</dt> <dt>

[Categorizando por recursos de componente](categorizing-by-component-capabilities.md)
</dt> <dt>

[Classes e associações padrão](default-classes-and-associations.md)
</dt> <dt>

[Definindo categorias de componentes](defining-component-categories.md)
</dt> <dt>

[O Gerenciador de categorias de componentes](the-component-categories-manager.md)
</dt> </dl>

 

 




