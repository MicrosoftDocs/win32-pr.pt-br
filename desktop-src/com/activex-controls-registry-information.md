---
title: Informações do registro de controles ActiveX
description: Informações do registro de controles ActiveX
ms.assetid: fda5b1e6-2048-4df7-ba8f-145652e3883c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6b180b327a4239b220185a9073ebc7bc0826c39
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104499161"
---
# <a name="activex-controls-registry-information"></a>Informações do registro de controles ActiveX

Há várias entradas de registro e sinalizadores que são usados. Além disso, os controles podem dar suporte a categorias de componentes para classificar os recursos que eles fornecem.

As chaves do registro relacionadas aos controles são marcadas com um asterisco na seguinte árvore:

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

A entrada **DefaultIcon** é usada para identificar um ícone a ser exibido quando o controle é minimizado para um ícone. A função [**ExtractIcon**](/windows/win32/api/shellapi/nf-shellapi-extracticona) é usada para obter o ícone do. DLL ou. Arquivo EXE especificado.

A entrada **ToolboxBitmap32** identifica o nome do módulo e o identificador de recurso para um bitmap de 16 \* 15 a ser usado para a face de uma barra de ferramentas ou botão de caixa de ferramentas. O tamanho do ícone padrão do Windows é muito grande para ser usado para essa finalidade. Essa entrada especificamente dá suporte a contêineres de controle que têm um modo de design no qual um seleciona os controles e os coloca em um formulário que está sendo criado. Por exemplo, em Visual Basic, o ícone do controle é exibido na caixa de ferramentas Visual Basic durante o modo de design.

A entrada de **controle** marca um objeto como um controle. Essa entrada é frequentemente usada por contêineres para preencher caixas de diálogo. O contêiner usa essa subchave para determinar se um objeto deve ser incluído em uma caixa de diálogo que exibe controles.

A subchave **insertável** também pode ser usada com controles, dependendo se o objeto pode agir somente como um objeto incorporado inserido sem recursos de controle especiais. Os objetos marcados com **insertáveis** aparecem na caixa de diálogo Inserir objeto de seu contêiner. A entrada **insertável** geralmente significa que o controle foi testado com contêineres que não são de controle.

As subchaves **insertáveis** e **Control** são opcionais. Um controle poderá omitir a subchave que pode ser **inserida** se não tiver sido projetada para trabalhar com contêineres mais antigos que não entendem controles. Um controle pode omitir a chave de **controle** se ele for projetado apenas para funcionar com um contêiner específico e, portanto, não desejar ser inserido em outros contêineres.

Os controles devem ter um verbo Properties, \_ Propriedades OLEIVERB, juntamente com quaisquer outros verbos aos quais eles dão suporte. O verbo Properties, bem como o verbo padrão OLEIVERB \_ principal, instrui o controle a exibir sua folha de propriedades. O verbo de propriedades é exibido como o item de propriedades no menu do contêiner quando o controle está ativo. Dessa forma, o controle pode exibir sua própria página de propriedades, permitindo uma funcionalidade útil para o usuário final, mesmo que o contêiner não manipule controles.

Um controle define a chave **MiscStatus** para se descrever para possíveis contêineres. Os bits assumem os valores de [**OLEMISC**](/windows/win32/api/oleidl/ne-oleidl-olemisc)e os controles adicionam vários valores a essa enumeração. Consulte os valores de enumeração **OLEMISC** para obter mais informações. O cliente pode obter essas informações chamando [**IOleObject:: GetMiscStatus**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getmiscstatus) sem precisar instanciar o controle primeiro.

Por fim, a **versão** descreve a versão do controle que deve corresponder à versão da biblioteca de tipos associada a este controle.

Também nas informações de tipo de um controle, o controle atributo marca uma entrada coclasse como descrevendo um controle.

 

 