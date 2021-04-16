---
description: Outra maneira de criar um namespace é usar o código formato MOF (MOF) para criar um namespace irmão. Um namespace irmão é um namespace que não existe como um filho do namespace atual.
ms.assetid: 1a3f8569-e725-4158-9a2b-b440b9247925
ms.tgt_platform: multiple
title: Criando um namespace irmão com código MOF
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4fcbf6e16ad51ab9a0df63e3497735b07cd6afc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105750567"
---
# <a name="creating-a-sibling-namespace-with-mof-code"></a>Criando um namespace irmão com código MOF

Outra maneira de criar um namespace é usar o código formato MOF (MOF) para criar um namespace irmão. Um namespace irmão é um namespace que não existe como um filho do namespace atual.

O procedimento a seguir descreve como criar um namespace irmão com código MOF.

**Para criar um namespace irmão com código MOF**

1.  Insira o comando de [**\# namespace pragma**](pragma-namespace.md) em seu código MOF antes da declaração do namespace.

    O comando [**\# pragma namespace**](pragma-namespace.md) instrui o WMI onde criar as instâncias seguindo a diretiva.

2.  Crie uma instância da classe [**\_ \_ namespace**](--namespace.md) .
3.  Compile seu código com o utilitário [Mofcomp](mofcomp.md) ou a interface [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) .

    Para obter mais informações, consulte [compilando arquivos MOF](compiling-mof-files.md).

O exemplo de código MOF a seguir descreve como criar um namespace como um irmão para o namespace "raiz \\ CIMv2".

``` syntax
#pragma namespace("\\\\.\\Root")

instance of __Namespace 
{
    Name = "MyNamespace";
};
```

 

 



