---
description: Acessando um valor de registro sem nome
ms.assetid: 1095da4c-8b9f-4674-9801-f2d25c4f372b
ms.tgt_platform: multiple
title: Acessando um valor de registro sem nome
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92860d240598f0353d1f4c9f41a77306942d272b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105786244"
---
# <a name="accessing-an-unnamed-registry-value"></a>Acessando um valor de registro sem nome

O valor padrão ou não nomeado de uma chave do registro é mostrado como (padrão) ou <No Name> no editor do registro do regedit. Você pode usar o provedor de registro do sistema para acessar uma chave de registro sem nome. Da mesma forma, você também pode usar o provedor de registro do sistema para acessar descrições de bitmap, que são definidas como valores não nomeados.

O procedimento a seguir descreve como recuperar um valor de registro sem nome.

**Para recuperar um valor de registro sem nome**

1.  Defina uma propriedade e defina o qualificador **PropertyContext** dessa propriedade como uma cadeia de caracteres vazia.

    O exemplo de código a seguir mostra como a classe define propriedades para armazenar valores para a chave especificada pelo qualificador **ClassContext** . O valor padrão é armazenado na propriedade **padrão** .

    ``` syntax
    [dynamic, 
     provider("RegProv"), 
     ClassContext("local|hkey_local_machine\\software\\"
     "microsoft\\Active Setup\\Installed Components")]

    class RegTrans{
      [key] String Transports="";
      [PropertyContext("")] String Default;
      [PropertyContext("ComponentId")] String ComponentID;
      [PropertyContext("Locale")] String Locale;
    };
    ```

    A chave de transportes não usa o valor sem nome, portanto, a compilação desse arquivo MOF não produz nenhum valor para a propriedade **padrão** , a menos que uma ferramenta de edição de registro seja usada para alterar o valor sem nome.

2.  Para um arquivo de bitmap, defina uma propriedade e defina o **PropertyContext** dessa propriedade.

    O exemplo de código a seguir mostra como definir uma propriedade.

    ```mof
    Local|hkey_classes_root\\.bmp
    ```

    

 

 



