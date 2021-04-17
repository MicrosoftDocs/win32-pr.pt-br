---
description: Explica como criar um controle de entrada matemática.
ms.assetid: 59976b01-9032-4226-a160-e9b2d4b8b23b
title: Criando um controle de entrada matemática
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5084f29943395bc6781fe20598f86bdc08c6c61
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104567028"
---
# <a name="creating-a-math-input-control"></a>Criando um controle de entrada matemática

Para criar o controle de entrada de matemática, você deve:

-   [Incluir cabeçalhos e bibliotecas para o controle de entrada matemática](#include-headers-and-libraries-for-the-math-input-control)
-   [Declare o ponteiro de controle e chame CoInitialize no ponteiro de controle](#declare-the-control-pointer-and-call-coinitialize-on-the-control-pointer)
-   [Mostrar o controle](#show-the-control)

## <a name="include-headers-and-libraries-for-the-math-input-control"></a>Incluir cabeçalhos e bibliotecas para o controle de entrada matemática

O código a seguir deve ser colocado na parte superior do seu código, em que você usará o controle de entrada de matemática.


```
   // includes for implementation
   #include "micaut.h"
   #include "micaut_i.c"
   
```



Esse código adicionará suporte para o controle de entrada matemática para seu aplicativo.

## <a name="declare-the-control-pointer-and-call-coinitialize-on-the-control-pointer"></a>Declare o ponteiro de controle e chame CoInitialize no ponteiro de controle

Depois de incluir os cabeçalhos para seu controle, você pode declarar o ponteiro de controle e pode chamar CoInitialize nele para criar um identificador para a interface de controle de entrada matemática. O código a seguir pode ser colocado em uma classe ou como uma variável global na implementação do seu aplicativo:


```
   CComPtr<IMathInputControl> g_spMIC; // Math Input Control
   
```



O código a seguir mostra como você pode chamar CoInitialize no ponteiro de controle.


```
   HRESULT hr = CoInitialize(NULL);
   hr = g_spMIC.CoCreateInstance(CLSID_MathInputControl);
   
```



Depois de chamar o CoInitialize no ponteiro de controle, você tem uma referência ao controle e pode acessar os métodos do controle. Por exemplo, você pode habilitar o conjunto estendido de controles, conforme mostrado no exemplo a seguir.


```
   hr = g_spMIC->EnableExtendedButtons(VARIANT_TRUE);
   
```



## <a name="show-the-control"></a>Mostrar o controle

O controle não será exibido automaticamente depois que você criá-lo. Para mostrar o controle, chame o método [**show**](/windows/desktop/api/micaut/nf-micaut-imathinputcontrol-show) na referência de controle que você criou na etapa anterior. O código a seguir demonstra como o método [**show**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow) pode ser chamado.


```
   hr = g_spMIC->Show();
   
```



Depois que o controle for exibido, ele será semelhante à ilustração a seguir.

![captura de tela mostrando o controle de entrada matemática](images/mic.png)

Observe que habilitei o conjunto estendido de botões para que **refazer** e **desfazer** estejam disponíveis.

 

 
