---
title: Práticas recomendadas para usar Cofre matrizes
description: Muitos métodos de interface do Microsoft Automação da Interface do Usuário \ 32; A API recebe argumentos chamados matrizes seguras do tipo de dados SAFEARRAY. Este tópico descreve as práticas recomendadas para usar matrizes seguras em Automação da Interface do Usuário aplicativos.
ms.assetid: 07e87cfd-d565-41b5-a68d-b99dd191fa95
keywords:
- Automação da Interface do Usuário, matrizes seguras
- Automação da Interface do Usuário,provedores
- Automação da Interface do Usuário,clientes
- Automação da Interface do Usuário, convertendo entre tipos de dados
- clientes, matrizes seguras
- providers,Automação da Interface do Usuário
- matrizes seguras
- tipos de dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39ea76358f3a547b4364d01f56e850d0cbb523fc35dfbaa2870448f70c6ad5ae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098116"
---
# <a name="best-practices-for-using-safe-arrays"></a>Práticas recomendadas para usar Cofre matrizes

Muitos métodos de interface da API do Microsoft Automação da Interface do Usuário levam argumentos chamados matrizes seguras, do tipo de dados [**SAFEARRAY.**](/windows/win32/api/oaidl/ns-oaidl-safearray) Este tópico descreve as práticas recomendadas para usar matrizes seguras em Automação da Interface do Usuário aplicativos.

## <a name="clients"></a>Clientes

Todas as matrizes seguras usadas com Automação da Interface do Usuário de API do cliente são matrizes unidimensionais baseadas em zero. Para criar uma matriz segura para um método de cliente Automação da Interface do Usuário, use a função [**SafeArrayCreateVector**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearraycreatevector) e, para ler e gravar em uma matriz segura, use as funções [**SafeArrayGetElement**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearraygetelement) e [**SafeArrayPutElement.**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearrayputelement) Quando você terminar de usar uma matriz segura, sempre a destruirá usando a função [**SafeArrayDestroy,**](/windows/desktop/api/oleauto/nf-oleauto-safearraydestroy) independentemente de você ter criado a matriz segura ou recebido de um método Automação da Interface do Usuário cliente.

Vários Automação da Interface do Usuário, incluindo métodos de recuperação de propriedade, como [**GetCurrentPropertyValue,**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue)recuperam [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant)s que podem conter estruturas [**POINT**](/previous-versions//dd162805(v=vs.85)) ou [**UiaRect.**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiarect) Um **POINT** é empacotado em **uma VARIANT** como uma matriz segura de doubles (VT R8) com o membro x no índice 0 e o membro y no índice \_ 1.    Da mesma forma, um **UiaRect** é empacotado em uma **VARIANT** como uma matriz segura de duplos com os membros à esquerda,  **superior,** largura e altura nos índices de 0 a 3, respectivamente.  Para uma matriz de **estruturas UiaRect,** a matriz segura contém uma matriz sequencial de quatro duplos para cada **UiaRect.** Os membros esquerdos ,  **superior,** **largura** e altura do primeiro **UiaRect** ocupam o índice de 0 a 3, os membros do segundo retângulo ocupam o índice de 4 a 7 e assim por diante.

A interface [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) inclui os métodos a seguir para converter entre [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) e vários outros tipos de dados.



| Método                                                                                               | Descrição                                                                                                     |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**IUIAutomation::IntNativeArrayToSafeArray**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-intnativearraytosafearray)   | Converte uma matriz de inteiros em [**um SAFEARRAY.**](/windows/win32/api/oaidl/ns-oaidl-safearray)                                          |
| [**IUIAutomation::IntSafeArrayToNativeArray**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-intsafearraytonativearray)   | Converte um [**SAFEARRAY de**](/windows/win32/api/oaidl/ns-oaidl-safearray) inteiros em uma matriz.                                          |
| [**IUIAutomation::SafeArrayToRectNativeArray**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-safearraytorectnativearray) | Converte um [**SAFEARRAY que**](/windows/win32/api/oaidl/ns-oaidl-safearray) contém coordenadas de retângulo em uma matriz do tipo **RECT**. |



 

## <a name="providers"></a>Provedores

Um provedor deve implementar vários métodos de interface que Automação da Interface do Usuário chamadas para recuperar informações do provedor. Muitas vezes, essas informações consistem em uma matriz de valores. Para retornar uma matriz para Automação da Interface do Usuário, o provedor deve empacotar a matriz em uma [**estrutura SAFEARRAY.**](/windows/win32/api/oaidl/ns-oaidl-safearray) Os elementos de matriz devem ser do tipo de dados esperado e devem aparecer na ordem esperada.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitual**
</dt> <dt>

[Visão geral das propriedades de automação da interface do usuário](uiauto-propertiesoverview.md)
</dt> <dt>

[Conceitos básicos de automação da interface do usuário](entry-uiautocore-overview.md)
</dt> </dl>

 

 