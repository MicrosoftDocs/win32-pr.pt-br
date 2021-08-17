---
title: ActiveX Controla informações do Registro
description: ActiveX Controla informações do Registro
ms.assetid: fda5b1e6-2048-4df7-ba8f-145652e3883c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87f062c11304c50161308cc5c6e43001c23f63486e60e568f61d6335f0947380
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117737380"
---
# <a name="activex-controls-registry-information"></a>ActiveX Controla informações do Registro

Há várias entradas e sinalizadores do Registro que são usados. Além disso, os controles podem dar suporte a categorias de componentes para classificar os recursos que eles fornecem.

As chaves do Registro relacionadas aos controles são marcadas com um asterisco na árvore a seguir:

```
HKEY_CLASSES_ROOT
   CLSID
      {control_CLSID}
         ProgID = <identifier>
         InprocServer32 = <filename>.dll
         *DefaultIcon = <filename>.<ext>,resourceID
         *ToolboxBitmap32 = <filename>.<ext>,resourceID
         *Control
         verb
            *n = &Properties...
         *MiscStatus = 0
         TypeLib = {object_typelibID}
         *Version = version_number
```

A **entrada DefaultIcon** é usada para identificar um ícone a ser exibido quando o controle é minimizado para um ícone. A [**função ExtractIcon**](/windows/win32/api/shellapi/nf-shellapi-extracticona) é usada para obter o ícone do arquivo .DLL ou .EXE especificado.

A **entrada ToolboxBitmap32** identifica o nome do módulo e o identificador de recurso para um bitmap de 16 15 a ser usado para o rosto de uma barra de ferramentas ou botão de \* caixa de ferramentas. O tamanho Windows ícone padrão é muito grande para ser usado para essa finalidade. Essa entrada dá suporte especificamente a contêineres de controle que têm um modo de design no qual um seleciona controles e os coloca em um formulário que está sendo projetado. Por exemplo, Visual Basic, o ícone do controle é exibido na caixa Visual Basic ferramentas durante o modo de design.

A **entrada Controle** marca um objeto como um controle . Essa entrada geralmente é usada por contêineres para preencher caixas de diálogo. O contêiner usa essa sub-chave para determinar se um objeto deve ser incluído em uma caixa de diálogo que exibe controles.

A  sub-chave Inserível também pode ser usada com controles, dependendo se o objeto pode agir apenas como um objeto inserido in-loco sem recursos de controle especiais. Objetos **marcados com Inserível** aparecem na caixa de diálogo Inserir Objeto do contêiner. A **entrada Inserível** geralmente significa que o controle foi testado com contêineres que não são de controle.

As **sub-chaves Insertable** e **Control** são opcionais. Um controle pode omitir **a** sub-chave Inserível se ele não foi projetado para funcionar com contêineres mais antigos que não entendem os controles. Um controle pode  omitir a chave de controle se ela só foi projetada para funcionar com um contêiner específico e, portanto, não deseja ser inserida em outros contêineres.

Os controles devem ter um verbo Properties, OLEIVERB \_ PROPERTIES, juntamente com todos os outros verbos que eles dão suporte. O verbo Propriedades, bem como o verbo padrão OLEIVERB PRIMARY, instrui o \_ controle a exibir sua folha de propriedades. O verbo Propriedades é exibido como o item Propriedades no menu do contêiner quando o controle está ativo. Dessa forma, o controle pode exibir sua própria página de propriedades, permitindo algumas funcionalidades úteis para o usuário final, mesmo se o contêiner não tratar controles.

Um controle define a **chave MiscStatus** para descrever a si mesmo para contêineres potenciais. Os bits usam os valores de [**OLEMISC**](/windows/win32/api/oleidl/ne-oleidl-olemisc)e os controles adicionam vários valores a essa enumeração. Consulte os **valores de enumeração OLEMISC** para obter mais informações. O cliente pode obter essas informações chamando [**IOleObject::GetMiscStatus**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getmiscstatus) sem precisar inciar o controle primeiro.

Por fim, **Version** descreve a versão do controle que deve corresponder à versão da biblioteca de tipos associada a esse controle.

Também nas informações de tipo para um controle , o controle de atributo marca uma entrada de coclasse como descrevendo um controle .

 

 