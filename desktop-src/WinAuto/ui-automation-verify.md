---
title: Automação da Interface do Usuário (Verificação de UIA)
description: Automação da Interface do Usuário (Verificação de UIA) é uma estrutura de teste para testes manuais e automatizados da implementação do controle ou do aplicativo da Microsoft Automação da Interface do Usuário.
ms.assetid: C66AF411-2746-4695-A893-1552B3ED1066
keywords:
- Verificação da Automação da Interface do Usuário
- Verificação de UIA
- Automação da Interface do Usuário implementação,teste
- Automação da Interface do Usuário
- Ferramentas de teste da UIA
- Automação da Interface do Usuário de teste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00f8c97d6522e353445ededff47a9a7cf123998b94f1323f1df59b7a380ac1d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052384"
---
# <a name="accessibility-tools---ui-automation-verify-uia-verify"></a>Ferramentas de acessibilidade – verificar Automação da Interface do Usuário (Verificação de UIA)

**Automação da Interface do Usuário (Verificação de UIA)** é uma estrutura de teste para testes manuais e automatizados da implementação de um controle ou aplicativo do Microsoft Automação da Interface do Usuário. A maioria das funcionalidades da estrutura de teste vem de uma DLL chamada WUIATestLibrary.dll. Essa DLL contém o código para testar Automação da Interface do Usuário funcionalidade específica e também dá suporte ao registro em log dos resultados do teste. Você pode integrar seu aplicativo ao código de teste e realizar testes regulares automatizados ou verificações spot de seus cenários Automação da Interface do Usuário dados.

**A UIA Verify** está instalada com o SDK (Software Development Kit) do Windows. Ele está localizado na pasta UIAVerify da plataforma de versão bin do caminho de instalação \\ \\ <  > \\ <  > \\ do SDK (VisualUIAVerifyNative.exe).

**A UIA Verify** consiste em uma API chamada biblioteca Automação da Interface do Usuário de teste e uma interface gui chamada Visual **Automação da Interface do Usuário Verify**. Eles são descritos nos tópicos a seguir.

> [!NOTE]
> **Automação da Interface do Usuário Verificar** é uma ferramenta herdado. Em vez disso, [recomendamos o uso Insights](https://accessibilityinsights.io/) acessibilidade.

## <a name="requirements"></a>Requisitos

Automação da Interface do Usuário deve estar presente no sistema. Para obter mais informações, consulte a seção "Requisitos" [do Automação da Interface do Usuário](entry-uiauto-win32.md).

**O UIA Verify** está instalado como parte do conjunto geral de ferramentas no SDK do Windows, ele não é distribuído como um download separado. O Windows SDK inclui todas as ferramentas relacionadas à acessibilidade documentadas nesta seção. [Obter o Windows SDK.](https://developer.microsoft.com/) (Também há um arquivo morto de download do SDK vinculado dessa página, se você precisar de uma versão anterior.)

Para executar **o UIA Verify** como uma ferramenta visual, encontre VisualUIAVerifyNative.exe na pasta \\ \\ <  > \\ UIAVerify da plataforma bin e execute-a (normalmente, você não precisa executar como administrador). Para obter mais informações, consulte [Visual Automação da Interface do Usuário Verify](visual-ui-automation-verify.md). Para usar as bibliotecas, consulte [Automação da Interface do Usuário Test Library](ui-automation-test-library.md).

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

 

 




