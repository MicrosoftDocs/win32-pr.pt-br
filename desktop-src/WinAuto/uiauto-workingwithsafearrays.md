---
title: Práticas recomendadas para usar matrizes seguras
description: Muitos métodos de interface da automação da interface do usuário da Microsoft \ 32; API usam argumentos chamados matrizes seguras, do tipo de dados SAFEARRAY. Este tópico descreve as práticas recomendadas para usar matrizes seguras em aplicativos de automação de interface do usuário.
ms.assetid: 07e87cfd-d565-41b5-a68d-b99dd191fa95
keywords:
- Automação da interface do usuário, matrizes seguras
- Automação da interface do usuário, provedores
- Automação da interface do usuário, clientes
- Automação da interface do usuário, convertendo entre tipos de dados
- clientes, matrizes seguras
- provedores, automação da interface do usuário
- matrizes seguras
- tipos de dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b12ade30398f8fbeb43336707f66a0709dfab83d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105812146"
---
# <a name="best-practices-for-using-safe-arrays"></a>Práticas recomendadas para usar matrizes seguras

Muitos métodos de interface da API de automação da interface do usuário da Microsoft levam argumentos chamados matrizes seguras, do tipo de dados [**SafeArray**](/windows/win32/api/oaidl/ns-oaidl-safearray) . Este tópico descreve as práticas recomendadas para usar matrizes seguras em aplicativos de automação de interface do usuário.

## <a name="clients"></a>Clientes

Todas as matrizes seguras que são usadas com os métodos de API do cliente de automação da interface do usuário são matrizes unidimensionais baseadas em zero. Para criar uma matriz segura para um método de cliente de automação da interface do usuário, use a função [**SafeArrayCreateVector**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearraycreatevector) e para ler e gravar em uma matriz segura, use as funções [**SafeArrayGetElement**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearraygetelement) e [**SafeArrayPutElement**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearrayputelement) . Quando você terminar de usar uma matriz segura, sempre a destruirá usando a função [**SafeArrayDestroy**](/windows/desktop/api/oleauto/nf-oleauto-safearraydestroy) , se você criou a matriz segura ou a recebeu de um método de cliente de automação da interface do usuário.

Vários métodos de automação da interface do usuário, incluindo métodos de recuperação de propriedade, como [**GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue), recuperam [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant)s que podem conter estruturas [**Point**](/previous-versions//dd162805(v=vs.85)) ou [**UiaRect**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiarect) . Um **ponto** é empacotado em uma **variante** como uma matriz segura de duplicatas (VT \_ R8) com o membro **x** no índice 0 e o membro **y** no índice 1. Da mesma forma, um **UiaRect** é empacotado em uma **variante** como uma matriz segura de duplicatas com os membros **esquerdo**, **superior**, **largura** e **altura** nos índices de 0 a 3, respectivamente. Para uma matriz de estruturas **UiaRect** , a matriz segura contém uma matriz sequencial de quatro duplos para cada **UiaRect**. Os membros **esquerdo**, **superior**, **largura** e **altura** do primeiro **UiaRect** ocupam o índice 0 até 3, os membros do segundo retângulo ocupam o índice 4 até 7 e assim por diante.

A interface [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) inclui os seguintes métodos para converter entre [**SafeArray**](/windows/win32/api/oaidl/ns-oaidl-safearray) e vários outros tipos de dados.



| Método                                                                                               | Descrição                                                                                                     |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**IUIAutomation::IntNativeArrayToSafeArray**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-intnativearraytosafearray)   | Converte uma matriz de inteiros em um [**SafeArray**](/windows/win32/api/oaidl/ns-oaidl-safearray).                                          |
| [**IUIAutomation::IntSafeArrayToNativeArray**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-intsafearraytonativearray)   | Converte um [**SafeArray**](/windows/win32/api/oaidl/ns-oaidl-safearray) de inteiros em uma matriz.                                          |
| [**IUIAutomation::SafeArrayToRectNativeArray**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-safearraytorectnativearray) | Converte um [**SafeArray**](/windows/win32/api/oaidl/ns-oaidl-safearray) que contém coordenadas de retângulo em uma matriz do tipo **Rect**. |



 

## <a name="providers"></a>Provedores

Um provedor deve implementar vários métodos de interface que a automação da interface do usuário chama para recuperar informações do provedor. Muitas vezes, essas informações consistem em uma matriz de valores. Para retornar uma matriz à automação da interface do usuário, o provedor deve empacotar a matriz em uma estrutura [**SafeArray**](/windows/win32/api/oaidl/ns-oaidl-safearray) . Os elementos da matriz devem ser do tipo de dados esperado e devem aparecer na ordem esperada.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Visão geral das propriedades de automação da interface do usuário](uiauto-propertiesoverview.md)
</dt> <dt>

[Conceitos básicos de automação da interface do usuário](entry-uiautocore-overview.md)
</dt> </dl>

 

 