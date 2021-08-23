---
description: Explica como criar um controle de entrada matemática.
ms.assetid: 59976b01-9032-4226-a160-e9b2d4b8b23b
title: Criando um Controle de Entrada de Expressões Matemáticas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ee8cca2a799bd44e79ef2f32691614bb3f22c933b40aa23dc4aa0cd6cfb6fb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967715"
---
# <a name="creating-a-math-input-control"></a>Criando um Controle de Entrada de Expressões Matemáticas

Para criar o controle de entrada matemática, você deve:

-   [Incluir headers e bibliotecas para o Controle de Entrada de Expressões Matemáticas](#include-headers-and-libraries-for-the-math-input-control)
-   [Declarar o ponteiro de controle e chamar CoInitialize no ponteiro de controle](#declare-the-control-pointer-and-call-coinitialize-on-the-control-pointer)
-   [Mostrar o controle](#show-the-control)

## <a name="include-headers-and-libraries-for-the-math-input-control"></a>Incluir headers e bibliotecas para o Controle de Entrada de Expressões Matemáticas

O código a seguir deve ser colocado na parte superior do código em que você estará usando o controle de entrada matemática.


```
   // includes for implementation
   #include "micaut.h"
   #include "micaut_i.c"
   
```



Esse código adicionará suporte para o controle de entrada matemática ao seu aplicativo.

## <a name="declare-the-control-pointer-and-call-coinitialize-on-the-control-pointer"></a>Declarar o ponteiro de controle e chamar CoInitialize no ponteiro de controle

Depois de incluir os headers para o controle, você pode declarar o ponteiro de controle e pode chamar CoInitialize nele para criar um alça para a interface de controle de entrada matemática. O código a seguir pode ser colocado em uma classe ou como uma variável global na implementação do aplicativo:


```
   CComPtr<IMathInputControl> g_spMIC; // Math Input Control
   
```



O código a seguir mostra como você pode chamar CoInitialize no ponteiro de controle.


```
   HRESULT hr = CoInitialize(NULL);
   hr = g_spMIC.CoCreateInstance(CLSID_MathInputControl);
   
```



Depois de chamar CoInitialize no ponteiro de controle, você tem uma referência ao controle e pode acessar os métodos do controle. Por exemplo, você pode habilitar o conjunto estendido de controles, conforme mostrado no exemplo a seguir.


```
   hr = g_spMIC->EnableExtendedButtons(VARIANT_TRUE);
   
```



## <a name="show-the-control"></a>Mostrar o controle

O controle não será exibido automaticamente depois que você o criar. Para mostrar o controle, chame o [**método Show**](/windows/desktop/api/micaut/nf-micaut-imathinputcontrol-show) na referência de controle que você criou na etapa anterior. O código a seguir demonstra como o [**método Show**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow) pode ser chamado.


```
   hr = g_spMIC->Show();
   
```



Depois que o controle aparecer, ele será parecido com a ilustração a seguir.

![captura de tela mostrando o controle de entrada matemática](images/mic.png)

Observe que habilitamos o conjunto estendido de botões para que **Refazer** e **Desfazer** estão disponíveis.

 

 
