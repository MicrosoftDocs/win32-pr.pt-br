---
description: Muitos aplicativos do painel de controle exibem uma folha de propriedades de propriedades para permitir que os usuários exibam e modifiquem várias configurações do dispositivo e do sistema.
title: Como registrar e implementar um manipulador de folha de propriedades para um aplicativo do painel de controle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47f7f8fe80bf5c7baceddac64d513d950378bcdf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828288"
---
# <a name="how-to-register-and-implement-a-property-sheet-handler-for-a-control-panel-application"></a>Como registrar e implementar um manipulador de folha de propriedades para um aplicativo do painel de controle

Muitos aplicativos do painel de controle exibem uma folha de propriedades de propriedades para permitir que os usuários exibam e modifiquem várias configurações do dispositivo e do sistema. Dois desses aplicativos — mouse e exibição — permitem que manipuladores de folha de propriedades substituam uma ou mais de suas páginas por uma página personalizada. A captura de tela a seguir mostra a folha de propriedades **Propriedades do mouse** .

![folha de propriedades propriedades do mouse](images/propsheethandler3.jpg)

Os manipuladores de folha de propriedades para aplicativos do painel de controle são semelhantes aos tipos de arquivo, com duas exceções principais:

-   Eles são chamados por um aplicativo do painel de controle, não pelo shell.
-   Elas são registradas de forma diferente.

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   Shell

### <a name="prerequisites"></a>Pré-requisitos

-   Uma compreensão do painel de controle
-   Uma compreensão dos menus de atalho

## <a name="instructions"></a>Instruções

### <a name="step-1-registering-a-property-sheet-handler-for-a-control-panel-application"></a>Etapa 1: registrar um manipulador de folha de propriedades para um aplicativo do painel de controle

Um manipulador de folhas de propriedades do aplicativo do painel de controle deve ser registrado na subchave do painel de controle. Essa chave pode estar em um dos dois locais, dependendo se o manipulador deve ser por usuário ou por computador. Para o registro por usuário, a subchave do painel de controle é **HKEY \_ Current \_ User** \\ **Control painel**. A macro REGSTR \_ Path \_ CONTROLPANEL, conforme definido em REGSTR. h, pode ser usada no código no lugar de "painel de controle". Para o registro por computador, o local é:

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            Current Version
               Controls Folder
```

Esse caminho pode ser referenciado no código como HKEY \_ local \_ Machine \\ REGSTR \_ Path \_ CONTROLSFOLDER, usando a \_ macro REGSTR Path \_ CONTROLSFOLDER que é definida em REGSTR. h.

Os aplicativos do painel de controle que permitem que os manipuladores de folhas de propriedades substituam páginas têm uma subchave na subchave do painel de controle, nomeada para o aplicativo, como mouse e exibição. A subchave do aplicativo deve ter uma subchave **shellex** com uma subchave **PropertySheetHandlers** . Para registrar um manipulador de folha de propriedades, adicione seu GUID à subchave **PropertySheetHandlers** que está associada ao aplicativo do painel de controle. Para fazer isso, crie uma subchave da subchave **PropertySheetHandlers** , chamada para o manipulador de folha de propriedades, e defina seu valor padrão como a forma de cadeia de caracteres do GUID do manipulador.

O exemplo a seguir registra um manipulador de folha de propriedades para o aplicativo do painel de controle do mouse em uma base por computador. Para registrá-lo em uma base por usuário, substitua **HKEY \_ local \_ Machine** \\ **REGSTR \_ caminho \_ CONTROLSFOLDER** com **HKEY \_ Current \_ User** \\ **REGSTR \_ Path \_ CONTROLPANEL**.

```
HKEY_LOCAL_MACHINE
   REGSTR_PATH_CONTROLSFOLDER
      Mouse
         shellex
            PropertySheetHandlers
               MyPropHandler
                  (Default) = {MyPropHandler CLSID GUID}
```

### <a name="step-2-implementing-a-property-sheet-handler-for-a-control-panel-application"></a>Etapa 2: Implementando um manipulador de folha de propriedades para um aplicativo do painel de controle

O procedimento para implementar um manipulador de folhas de propriedades do painel de controle é muito semelhante ao que foi discutido em [como registrar e implementar um manipulador de folha de propriedades para um tipo de arquivo](how-to-register-and-implement-a-property-sheet-handler-for-a-file-type.md). A principal diferença é que agora [**IShellPropSheetExt:: ReplacePage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage) precisa de uma implementação não token em vez de [**IShellPropSheetExt:: AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages).

Quando um aplicativo do painel de controle está prestes a exibir sua folha de propriedades, ele chama o método [**IShellPropSheetExt:: ReplacePage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage) do manipulador de folhas de propriedades uma vez para cada página que pode ser substituída. O parâmetro *uPageID* é definido como a ID da página. As IDs para as páginas disponíveis são definidas em Cplext. h. As IDs disponíveis no momento estão listadas na tabela a seguir. 

| ID da página                      | Description         | Aplicativo do painel de controle |
|------------------------------|---------------------|---------------------------|
| CPLPAGE \_ botões de mouse \_      | A página botões    | Mouse                     |
| CPLPAGE \_ mouse \_ PTRMOTION    | A página de movimento     | Mouse                     |
| \_roda do mouse CPLPAGE \_        | A página de roda      | Mouse                     |
| \_velocidade do teclado CPLPAGE \_     | A página velocidade      | Keyboard                  |
| \_tela de \_ fundo do CPLPAGE | A página de plano de fundo | Monitor                   |



 

## <a name="remarks"></a>Comentários

O procedimento para criar e substituir uma página é idêntico ao da adição de uma página. Para obter mais informações, consulte [como registrar e implementar um manipulador de folha de propriedades para um tipo de arquivo](how-to-register-and-implement-a-property-sheet-handler-for-a-file-type.md).

 

 



