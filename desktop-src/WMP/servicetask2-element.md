---
title: Elemento ServiceTask2
description: Observação Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online. O elemento ServiceTask2 representa o segundo painel de tarefas da loja online.
ms.assetid: f920ef25-efca-47c8-bcbc-2cb34593e879
keywords:
- Elemento ServiceTask2 do Windows Media Player
topic_type:
- apiref
api_name:
- ServiceTask2 Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 36052dabc1be7f2925f5185239faa602b8633fc6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747285"
---
# <a name="servicetask2-element"></a>Elemento ServiceTask2

> [!Note]  
> Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

O elemento **ServiceTask2** representa o segundo painel de tarefas da loja online.

``` syntax
<ServiceTask2
    URL = "URL"
/>
```

## <a name="attributes"></a>Atributos



| Termo                                                                                                                             | Descrição                                                        |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span id="URL__required_"></span><span id="url__required_"></span><span id="URL__REQUIRED_"></span>**URL** (obrigatório)<br/> | URL da página da Web exibida pelo Windows Media Player.<br/> |



 

## <a name="parentchild-elements"></a>Elementos pai/filho



| Hierarquia       | Elemento                       |
|-----------------|-------------------------------|
| Elementos pai | **ServiceInfo**               |
| Elementos filho  | **ButtonText**, **ButtonTip** |



 

## <a name="remarks"></a>Comentários

**ServiceTask1** é considerado o painel de tarefas principal para envolvimento em atividades comerciais. É o painel de tarefas exibido quando o usuário escolhe comprar música. Use **ServiceTask2** para outra atividade de loja online.

> [!Note]  
> O Windows Media Player 10 tem três painéis de tarefas em que um repositório online pode exibir suas páginas da Web. O repositório online pode optar por usar um, dois ou todos os três painéis de tarefas. O Windows Media Player 11 tem apenas um painel de tarefas, que pode ser exibido pelo usuário clicando na guia **lojas online** . o Windows Media Player 11 ignora os elementos **ServiceTask2** e **ServiceTask3** .

 

Os painéis de tarefas de lojas online compartilham uma única instância do navegador. Isso significa que você não deve escrever o código de script em sua página da Web que você espera que continue a ser executado quando o usuário mudar para a tarefa de serviço atual.

Quando o usuário alterna os painéis de tarefas, o Windows Media Player armazena a URL e os cookies de sessão. Quando o usuário volta ao painel de tarefas, o Player restaura a URL e os cookies. Se o usuário optar por usar uma loja online diferente, os dados da URL e da sessão serão apagados.

A tabela a seguir detalha os parâmetros enviados com a solicitação de URL. Outros podem estar presentes para fins de compatibilidade herdada.



| Nome         | Valor                                                                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *GeoId*      | ID da localização geográfica do Windows. A ID de local é especificada pelo usuário na área **local** das configurações de opções regionais e de idiomas no painel de controle. |
| *locale*     | ID de localidade do Windows Media Player.                                                                                                                                     |
| *UserLocale* | IDENTIFICAÇÃO de localidade do Windows. A localidade é especificada pelo usuário na área **padrões e formatos** das configurações de opções regionais e de idiomas no painel de controle.        |
| *version*    | Número de versão do Windows Media Player usando o seguinte formato: 10.0. x. xxxx ou 11.0. x. xxxx.                                                                         |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------|
| Versão<br/> | Windows Media Player 10 ou posterior.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Documento de informações de exemplo para uma loja online tipo 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Documento de informações de exemplo para uma loja online tipo 2**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Documento do serviceInfo**](serviceinfo-document.md)
</dt> </dl>

 

 





