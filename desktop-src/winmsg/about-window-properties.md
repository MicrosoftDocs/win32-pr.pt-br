---
description: Esta visão geral aborda as propriedades da janela.
ms.assetid: 67ca264e-af8e-41bf-b9d1-d3db8cf1cdc3
title: Sobre propriedades da janela
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c88657cba4cf12ed7ecedb07aeb545f8e4bf64109d34297637d734743d32dd2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028494"
---
# <a name="about-window-properties"></a>Sobre propriedades da janela

Uma *propriedade de* janela é qualquer dado atribuído a uma janela. Uma propriedade de janela geralmente é um lidar com os dados específicos da janela, mas pode ser qualquer valor. Cada propriedade de janela é identificada por um nome de cadeia de caracteres. Há várias funções que permitem que os aplicativos usem propriedades de janela. Esta visão geral aborda os seguintes tópicos:

-   [Vantagens de usar propriedades de janela](#advantages-of-using-window-properties)
-   [Atribuindo propriedades de janela](#assigning-window-properties)
-   [Enumerando propriedades da janela](#enumerating-window-properties)

## <a name="advantages-of-using-window-properties"></a>Vantagens de usar propriedades de janela

As propriedades da janela normalmente são usadas para associar dados a uma janela de subclasse ou a uma janela em um aplicativo MDI (interface de vários documentos). Em ambos os casos, não é conveniente usar os bytes extras especificados na estrutura de classe ou função [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) pelos dois motivos a seguir:

-   Um aplicativo pode não saber quantos bytes extras estão disponíveis ou como o espaço está sendo usado. Usando propriedades de janela, o aplicativo pode associar dados a uma janela sem acessar os bytes extras.
-   Um aplicativo deve acessar os bytes extras usando deslocamentos. No entanto, as propriedades da janela são acessadas por seus identificadores de cadeia de caracteres, não por deslocamentos.

Para obter mais informações sobre subclasse, consulte [Subclasse de procedimento de janela](about-window-procedures.md). Para obter mais informações sobre janelas MDI, consulte [Interface de vários documentos.](multiple-document-interface.md)

## <a name="assigning-window-properties"></a>Atribuindo propriedades de janela

A [**função SetProp**](/windows/win32/api/winuser/nf-winuser-setpropa) atribui uma propriedade de janela e seu identificador de cadeia de caracteres a uma janela. A [**função GetProp**](/windows/win32/api/winuser/nf-winuser-getpropa) recupera a propriedade de janela identificada pela cadeia de caracteres especificada. A [**função RemoveProp**](/windows/win32/api/winuser/nf-winuser-removepropa) destrói a associação entre uma janela e uma propriedade de janela, mas não destrói os dados em si. Para destruir os dados em si, use a função apropriada para liberar o alça que é retornado por **RemoveProp**.

## <a name="enumerating-window-properties"></a>Enumerando propriedades da janela

As [**funções EnumProps**](/windows/win32/api/winuser/nf-winuser-enumpropsa) [**e EnumPropsEx**](/windows/win32/api/winuser/nf-winuser-enumpropsexa) enumeram todas as propriedades de uma janela usando uma função de retorno de chamada definida pelo aplicativo. Para obter mais informações sobre a função de retorno de chamada, [*consulte PropEnumProc*](/windows/win32/api/winuser/nc-winuser-propenumproca).

[**EnumPropsEx**](/windows/win32/api/winuser/nf-winuser-enumpropsexa) inclui um parâmetro extra para dados definidos pelo aplicativo usados pela função de retorno de chamada. Para obter mais informações sobre a função de retorno de chamada, [*consulte PropEnumProcEx*](/windows/win32/api/winuser/nc-winuser-propenumprocexa).

 

 
