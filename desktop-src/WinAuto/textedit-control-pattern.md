---
title: Padrão de controle TextEdit
description: Apresenta diretrizes e convenções para implementar ITextEditProvider, incluindo informações sobre propriedades e métodos.
ms.assetid: AA9E04AC-1AC0-6434-ADEF-9FF82ADA7CD9
keywords:
- Automação da Interface do Usuário, implementando o padrão de controle TextEdit
- Automação da Interface do Usuário, padrão de controle TextEdit
- padrões de controle, TextEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc30701639301a49f23637067f5c8666f13b0276de4133e151b5e528af1f1ae1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118827796"
---
# <a name="textedit-control-pattern"></a>Padrão de controle TextEdit

Apresenta diretrizes e convenções para implementar [**ITextEditProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itexteditprovider), incluindo informações sobre propriedades e métodos. O **padrão de controle TextEdit** é usado para acesso programático a um controle que modifica o texto, por exemplo, um controle que executa a correção automática ou habilita a composição de entrada.

> [!Note]  
> As notas de implementação neste tópico referem-se a APIs que vêm Estrutura de Serviços de Texto (TSF). Para obter mais informações sobre o TSF e a referência de API, [consulte Estrutura de Serviços de Texto](/windows/desktop/TSF/text-services-framework).

 

## <a name="required-members-for-itexteditprovider"></a>Membros necessários para **ITextEditProvider**

Essas propriedades e métodos são necessários para implementar a interface [**ITextEditProvider.**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itexteditprovider)



| Membros necessários                                                              | Tipo de membro | Observações                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetActiveComposition**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itexteditprovider-getactivecomposition) | Método      | Retorna o intervalo da conversão atual (nenhum se não houver conversão). Retornar a composição ativa (no TSF, esse é o intervalo marcado por **GUID \_ PROP \_ COMPOSING**). Por exemplo, com o IME (Editor de Método de Entrada Japonês) da Microsoft, esse seria o texto sublinhado completo. |
| [**GetConversionTarget**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itexteditprovider-getconversiontarget)   | Método      | Retorna o intervalo de destino de conversão atual (nenhum se nenhuma conversão). No TSF, esse é o intervalo de caracteres marcados como **TF \_ ATTR \_ TARGET \_ NOTCONVERTED** ou **TF \_ ATTR \_ TARGET \_ CONVERTIDA** da estrutura **TF \_ DISPLAYATTRIBUTE.**                                               |



 

Os **eventos TextEditTextChanged** e **ConversionTargetChanged** devem ser gerados pelos elementos Automação da Interface do Usuário Microsoft que suportam o padrão **TextEdit.**

### <a name="textedittextchanged"></a>**TextEditTextChanged**

-   Use a [**função UiaRaiseTextEditTextChangedEvent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraisetextedittextchangedevent) para auviar **o evento TextEditTextChanged.**
-   A tabela a seguir lista os casos em que você deve auviar o evento e os parâmetros [**UiaRaiseTextEditTextChangedEvent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraisetextedittextchangedevent) a usar.



| TextEditChangeType                                            | Carga do evento                                | Observações                                                                                                                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------|----------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Autocorreção**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-texteditchangetype)          | Nova cadeia de caracteres corrigida                         | Gerado quando uma correção automática é feita pelo controle . Ou sempre que uma substituição for feita por meio do TSF e o intervalo tiver um **valor GUID \_ PROP \_ TKB \_ ALTERNATES** de **TKB \_ ALTERNATES \_ AUTOCORRECTION \_ APLICADO.**<br/>                                                                                                                                                                   |
| [**Composição**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-texteditchangetype)          | A cadeia de caracteres atualizada                           | O payload só deve incluir os caracteres que foram alterados (não envie toda a cadeia de caracteres de composição). Gerado sempre que uma substituição de composição é feita. No TSF, uma substituição de composição é definida como uma substituição que tem o **sinalizador GUID \_ PROP \_ COMPOSING** definido. Editar controles que implementam o TSF pode monitorar essas alterações por meio da **notificação OnEndEdit.**<br/>         |
| [**CompositionFinalized**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-texteditchangetype) | A cadeia de caracteres de composição finalizada (consulte Observações) | No TSF, a cadeia de caracteres de conversão que está sendo finalizada é definida pelo **sinalizador \_ GUID PROP \_ COMPOSING** que está sendo removido de uma composição. Os controles de edição que implementam o TSF devem determinar a cadeia de caracteres finalizada de **EndComposition** e acionar o evento **quando OnEndEdit** for chamado.<br/> A cadeia de caracteres de composição finalizada poderá estar vazia se a composição tiver sido cancelada ou excluída.<br/> |



 

### <a name="conversiontargetchanged"></a>**ConversionTargetChanged**

-   **ConversionTargetChanged ocorre** quando o destino de conversão muda de um destino para outro.
-   Use a [**função UiaRaiseAutomationEvent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraiseautomationevent) para gerar o evento **ConversionTargetChanged** (passe o identificador de evento [**\_ UIA TextEdit \_ ConversionTargetChangedEventId).**](https://www.bing.com/search?q=**UIA\_TextEdit\_ConversionTargetChangedEventId**)
-   **ConversionTargetChanged** não deve ser gerado quando o conteúdo do destino é alterado. Se a alteração de destino ocorrer simultaneamente com uma alteração de composição, o evento de alteração de destino deverá ser gerado depois que qualquer evento de composição já tiver sido gerado.
-   No TSF, o destino de conversão é definido pelo valor **TF \_ ATTR \_ TARGET \_ CONVERT** que está sendo definido da estrutura **TF \_ DISPLAYATTRIBUTE.** As alterações podem ser monitoradas **usando OnEndEdit**.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitual**
</dt> <dt>

[Tipos de controle e seus padrões de controle com suporte](uiauto-controlpatternmapping.md)
</dt> <dt>

[Visão Geral de Padrões de Controle de Automação de Interface de Usuário](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Visão geral da árvore de automação de interface do usuário](uiauto-treeoverview.md)
</dt> </dl>

 

