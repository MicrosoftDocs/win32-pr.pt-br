---
title: Verificação de automação da interface do usuário (UIA verificar)
description: A verificação de automação da interface do usuário (UIA Verify) é uma estrutura de teste para teste manual e automatizado da implementação de um controle ou do aplicativo da automação da interface do usuário da Microsoft.
ms.assetid: C66AF411-2746-4695-A893-1552B3ED1066
keywords:
- Verificação da Automação da Interface do Usuário
- Verificação de UIA
- Implementação da automação da interface do usuário, teste
- testando a automação da interface do usuário
- Ferramentas de teste de UIA
- Ferramentas de teste de automação da interface do usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b794e5d191c07a9c0db602ebac0f908bbdf960bf
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104365649"
---
# <a name="accessibility-tools---ui-automation-verify-uia-verify"></a>Ferramentas de acessibilidade – verificação de automação da interface do usuário (UIA verificar)

A **verificação de automação da interface do usuário (UIA Verify)** é uma estrutura de teste para teste manual e automatizado da implementação de um controle ou do aplicativo da automação da interface do usuário da Microsoft. A maioria das funcionalidades da estrutura de teste vem de uma DLL chamada WUIATestLibrary.dll. Essa DLL contém o código para testar a funcionalidade de automação da interface do usuário específica e também dá suporte ao registro em log dos resultados do teste. Você pode integrar seu aplicativo no código de teste e realizar verificações regulares, automatizadas ou comparações de testes de seus cenários de automação da interface do usuário.

O **UIA Verify** é instalado com o SDK (Software Development Kit) do Windows. Ele está localizado na \\ pasta bin \\ < *version* > \\ <  > \\ UIAVerify do caminho de instalação do SDK (VisualUIAVerifyNative.exe).

A **verificação de UIA** consiste em uma API chamada biblioteca de teste de automação da interface do usuário e uma interface GUI chamada **verificação da automação da interface do usuário** Visual. Eles são descritos nos tópicos a seguir.

> [!NOTE]
> A **verificação de automação da interface do usuário** é uma ferramenta herdada. Em vez disso, recomendamos o uso de [informações de acessibilidade](https://accessibilityinsights.io/) .

## <a name="requirements"></a>Requisitos

A automação da interface do usuário deve estar presente no sistema. Para obter mais informações, consulte a seção "requisitos" da [automação da interface do usuário](entry-uiauto-win32.md).

A **verificação de UIA** é instalada como parte do conjunto geral de ferramentas no SDK do Windows, ela não é distribuída como um download separado. O SDK do Windows inclui todas as ferramentas relacionadas à acessibilidade documentadas nesta seção. [Obtenha o SDK do Windows.](https://developer.microsoft.com/) (Há também um arquivo de download do SDK vinculado dessa página, se você precisar de uma versão anterior.)

Para executar o **UIA Verify** como uma ferramenta Visual, localize VisualUIAVerifyNative.exe na \\ pasta bin \\ < *Platform* > \\ UIAVerify e execute-o (normalmente, você não precisa executar como administrador). Para obter mais informações, consulte [Visual IU Automation Verify](visual-ui-automation-verify.md). Para usar as bibliotecas, consulte [biblioteca de teste de automação da interface do usuário](ui-automation-test-library.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Accessible Event Watcher](accessible-event-watcher.md)
</dt> <dt>

[Inspecionar](inspect-objects.md)
</dt> <dt>

[Ferramentas de teste](testing-tools.md)
</dt> <dt>

[UI Accessibility Checker](ui-accessibility-checker.md)
</dt> </dl>

 

 




