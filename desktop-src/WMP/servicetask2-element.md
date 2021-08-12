---
title: Elemento ServiceTask2
description: Observação Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online. O elemento ServiceTask2 representa o segundo painel de tarefas da loja online.
ms.assetid: f920ef25-efca-47c8-bcbc-2cb34593e879
keywords:
- Elemento ServiceTask2 Windows Media Player
topic_type:
- apiref
api_name:
- ServiceTask2 Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5b1d56001effab8ae4f7375023aeac48936f7e2faeb9806b43ca90d3292b82e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118569744"
---
# <a name="servicetask2-element"></a>Elemento ServiceTask2

> [!Note]  
> Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

O **elemento ServiceTask2** representa o segundo painel de tarefas da loja online.

``` syntax
<ServiceTask2
    URL = "URL"
/>
```

## <a name="attributes"></a>Atributos



| Termo                                                                                                                             | Descrição                                                        |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span id="URL__required_"></span><span id="url__required_"></span><span id="URL__REQUIRED_"></span>**URL** (obrigatório)<br/> | URL para a página da Web Windows Media Player exibida.<br/> |



 

## <a name="parentchild-elements"></a>Elementos pai/filho



| Hierarquia       | Elemento                       |
|-----------------|-------------------------------|
| Elementos pai | **ServiceInfo**               |
| Elementos filho  | **ButtonText,** **ButtonTip** |



 

## <a name="remarks"></a>Comentários

**ServiceTask1 é** considerado o painel de tarefas principal para participar da atividade comercial. É o painel de tarefas que é exibido quando o usuário opta por comprar música. Use **ServiceTask2 para** outra atividade de loja online.

> [!Note]  
> Windows Media Player 10 tem três painéis de tarefas em que uma loja online pode exibir suas páginas da Web. A loja online pode optar por usar um, dois ou todos os três painéis de tarefas. Windows Media Player 11 tem apenas um painel de tarefas, que o usuário pode exibir clicando na guia **Lojas Online.** O Windows Media Player 11 ignora os elementos **ServiceTask2** e **ServiceTask3.**

 

Os painéis de tarefas de lojas online compartilham uma única instância do navegador. Isso significa que você não deve escrever código de script em sua página da Web que você espera continuar a ser executado quando o usuário alterna da tarefa de serviço atual.

Quando o usuário alterna os painéis de tarefas, Windows Media Player armazena a URL e os cookies de sessão. Quando o usuário alterna de volta para o painel de tarefas, o Player restaura a URL e os cookies. Se o usuário optar por usar um armazenamento online diferente, os dados da URL e da sessão serão limpos.

A tabela a seguir detalha os parâmetros enviados com a solicitação de URL. Outros podem estar presentes para fins de compatibilidade herdado.



| Name         | Valor                                                                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Geoid*      | Windows ID de localização geográfica. A ID de local é especificada pelo usuário na **área** Local das configurações De Opções Regionais e de Idioma Painel de Controle. |
| *locale*     | Windows Media Player ID da localidade.                                                                                                                                     |
| *userlocale* | Windows ID de localidade. A localidade é especificada pelo usuário na área Padrões e **Formatos** das configurações Opções Regionais e de Idioma Painel de Controle.        |
| *version*    | Windows Media Player número de versão usando o seguinte formato: 10.0.x.xxxx ou 11.0.x.xxxx.                                                                         |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------|
| Versão<br/> | Windows Media Player 10 ou posterior.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Documento ServiceInfo de exemplo para uma loja online do tipo 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Documento ServiceInfo de exemplo para uma loja online do tipo 2**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Documento ServiceInfo**](serviceinfo-document.md)
</dt> </dl>

 

 





