---
description: Esta visão geral discute as propriedades da janela.
ms.assetid: 67ca264e-af8e-41bf-b9d1-d3db8cf1cdc3
title: Sobre as propriedades da janela
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea646c594186b05bb74e70e6829f13a83cd0ec1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169569"
---
# <a name="about-window-properties"></a>Sobre as propriedades da janela

Uma *propriedade de janela* é qualquer dado atribuído a uma janela. Uma propriedade de janela geralmente é um identificador dos dados específicos da janela, mas pode ser qualquer valor. Cada propriedade de janela é identificada por um nome de cadeia de caracteres. Há várias funções que permitem que os aplicativos usem Propriedades de janela. Esta visão geral aborda os seguintes tópicos:

-   [Vantagens do uso de propriedades de janela](#advantages-of-using-window-properties)
-   [Atribuindo Propriedades de janela](#assigning-window-properties)
-   [Enumerando Propriedades da janela](#enumerating-window-properties)

## <a name="advantages-of-using-window-properties"></a>Vantagens do uso de propriedades de janela

As propriedades da janela normalmente são usadas para associar dados a uma janela de subclasse ou a uma janela em um aplicativo MDI (interface de vários documentos). Em ambos os casos, não é conveniente usar os bytes extras especificados na função [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) ou estrutura de classe pelos dois motivos a seguir:

-   Um aplicativo talvez não saiba quantos bytes extras estão disponíveis ou como o espaço está sendo usado. Usando as propriedades da janela, o aplicativo pode associar dados a uma janela sem acessar os bytes extras.
-   Um aplicativo deve acessar os bytes extras usando deslocamentos. No entanto, as propriedades da janela são acessadas por seus identificadores de cadeia de caracteres, não por deslocamentos.

Para obter mais informações sobre subclasses, consulte [subclasse de procedimento de janela](about-window-procedures.md). Para obter mais informações sobre janelas MDI, consulte [várias interfaces de documento](multiple-document-interface.md).

## <a name="assigning-window-properties"></a>Atribuindo Propriedades de janela

A função [**SetProp**](/windows/win32/api/winuser/nf-winuser-setpropa) atribui uma Propriedade Window e seu identificador de cadeia de caracteres a uma janela. A função [**GetProp**](/windows/win32/api/winuser/nf-winuser-getpropa) recupera a Propriedade Window identificada pela cadeia de caracteres especificada. A função [**RemoveProp**](/windows/win32/api/winuser/nf-winuser-removepropa) destrói a associação entre uma janela e uma propriedade de janela, mas não destrói os dados em si. Para destruir os dados em si, use a função apropriada para liberar o identificador retornado por **RemoveProp**.

## <a name="enumerating-window-properties"></a>Enumerando Propriedades da janela

As funções [**EnumProps**](/windows/win32/api/winuser/nf-winuser-enumpropsa) e [**EnumPropsEx**](/windows/win32/api/winuser/nf-winuser-enumpropsexa) enumeram todas as propriedades de uma janela usando uma função de retorno de chamada definida pelo aplicativo. Para obter mais informações sobre a função de retorno de chamada, consulte [*PropEnumProc*](/windows/win32/api/winuser/nc-winuser-propenumproca).

[**EnumPropsEx**](/windows/win32/api/winuser/nf-winuser-enumpropsexa) inclui um parâmetro extra para dados definidos pelo aplicativo usados pela função de retorno de chamada. Para obter mais informações sobre a função de retorno de chamada, consulte [*PropEnumProcEx*](/windows/win32/api/winuser/nc-winuser-propenumprocexa).

 

 
