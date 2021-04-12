---
title: Padrão de controle editor
description: Apresenta diretrizes e convenções para implementar ITextEditProvider, incluindo informações sobre propriedades e métodos.
ms.assetid: AA9E04AC-1AC0-6434-ADEF-9FF82ADA7CD9
keywords:
- Automação da interface do usuário, implementando o padrão de controle editor
- Automação da interface do usuário, padrão de controle editor
- padrões de controle, editor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdf8512db4f676a263bf46bdbdfea7b6b7eaba11
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294464"
---
# <a name="textedit-control-pattern"></a>Padrão de controle editor

Apresenta diretrizes e convenções para implementar [**ITextEditProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itexteditprovider), incluindo informações sobre propriedades e métodos. O padrão de controle **Editor** é usado para acesso programático a um controle que modifica o texto, por exemplo, um controle que executa a correção automática ou habilita a composição de entrada.

> [!Note]  
> As notas de implementação neste tópico referem-se às APIs que vêm da TSF (Text Services Framework). Para obter mais informações sobre o TSF e a referência de API, consulte [estrutura de serviços de texto](/windows/desktop/TSF/text-services-framework).

 

## <a name="required-members-for-itexteditprovider"></a>Membros necessários para **ITextEditProvider**

Essas propriedades e métodos são necessários para implementar a interface [**ITextEditProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itexteditprovider) .



| Membros necessários                                                              | Tipo de membro | Observações                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetActiveComposition**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itexteditprovider-getactivecomposition) | Método      | Retorna o intervalo da conversão atual (nenhum se não houver conversão). Retornar a composição ativa (no TSF, esse é o intervalo marcado por **\_ \_ composição de prop de GUID**). Por exemplo, com o IME (editor de método de entrada) do Microsoft Japanese, esse seria o texto sublinhado completo. |
| [**GetConversionTarget**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itexteditprovider-getconversiontarget)   | Método      | Retorna o intervalo de destino da conversão atual (nenhum se nenhuma conversão). No TSF, esse é o intervalo de caracteres marcados como **TF \_ attr \_ target não \_ convertido** ou **TF \_ attr \_ target \_ convertido** da estrutura **TF \_ DisplayAttribute** .                                               |



 

Os eventos **TextEditTextChanged** e **ConversionTargetChanged** devem ser gerados por elementos de automação da interface do usuário da Microsoft que dão suporte ao padrão **Editor** .

### <a name="textedittextchanged"></a>**TextEditTextChanged**

-   Use a função [**UiaRaiseTextEditTextChangedEvent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraisetextedittextchangedevent) para gerar o evento **TextEditTextChanged** .
-   A tabela a seguir lista os casos em que você deve gerar o evento e os parâmetros [**UiaRaiseTextEditTextChangedEvent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraisetextedittextchangedevent) a serem usados.



| TextEditChangeType                                            | Carga do evento                                | Observações                                                                                                                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------|----------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Matemática**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-texteditchangetype)          | Nova cadeia de caracteres corrigida                         | Gerado quando uma correção automática é feita pelo controle. Ou sempre que uma substituição é feita por meio de TSF e o intervalo tem um valor da **GUID \_ prop \_ TKB \_ alternativos** de **TKB \_ alterna a \_ correção automática \_ aplicada**.<br/>                                                                                                                                                                   |
| [**Composição**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-texteditchangetype)          | A cadeia de caracteres atualizada                           | A carga deve incluir apenas os caracteres que foram alterados (não envie a cadeia de caracteres de composição inteira). Gerado sempre que uma substituição de composição é feita. No TSF, uma substituição de composição é definida como uma substituição que tem o sinalizador de **\_ \_ composição prop do GUID** definido. Os controles de edição que implementam o TSF podem monitorar essas alterações por meio da notificação **onendedit** .<br/>         |
| [**CompositionFinalized**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-texteditchangetype) | A cadeia de caracteres de composição finalizada (consulte Observações) | No TSF, a cadeia de caracteres de conversão que está sendo finalizada é definida pelo sinalizador de **\_ \_ composição de props de GUID** que está sendo removido de uma composição. Os controles de edição que implementam o TSF devem determinar a cadeia de caracteres finalizada de **endcomposição** e gerar o evento quando **onendedit** é chamado.<br/> A cadeia de caracteres de composição finalizada poderá estar vazia se a composição tiver sido cancelada ou excluída.<br/> |



 

### <a name="conversiontargetchanged"></a>**ConversionTargetChanged**

-   **ConversionTargetChanged** ocorre quando o destino da conversão é alterado de um destino para outro.
-   Use a função [**UiaRaiseAutomationEvent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraiseautomationevent) para gerar o evento **ConversionTargetChanged** (passe o identificador de evento [**UIA \_ Editor \_ ConversionTargetChangedEventId**](https://www.bing.com/search?q=**UIA\_TextEdit\_ConversionTargetChangedEventId**) ).
-   **ConversionTargetChanged** não deve ser gerado quando o conteúdo do destino é alterado. Se a alteração de destino ocorrer simultaneamente com uma alteração de composição, o evento de alteração de destino deverá ser gerado depois que qualquer evento de composição já tiver sido gerado.
-   No TSF, o destino da conversão é definido pelo valor **TF \_ attr \_ target \_ convertido** sendo definido da estrutura **TF \_ DisplayAttribute** . As alterações podem ser monitoradas usando o **onendedit**.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Tipos de controle e seus padrões de controle com suporte](uiauto-controlpatternmapping.md)
</dt> <dt>

[Visão Geral de Padrões de Controle de Automação de Interface de Usuário](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Visão geral da árvore de automação de interface do usuário](uiauto-treeoverview.md)
</dt> </dl>

 

