---
title: Elemento ServiceTask3
description: Observação Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online. O elemento ServiceTask3 representa o terceiro painel de tarefas da loja online.
ms.assetid: 3d08f9ff-d75b-4967-90f8-23ab71d38883
keywords:
- Windows Media Player do elemento ServiceTask3
topic_type:
- apiref
api_name:
- ServiceTask3 Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0c53ef9eb4a758e47d639446750465934fb4a6c031d8abd387276add2f0df519
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119763626"
---
# <a name="servicetask3-element"></a>Elemento ServiceTask3

> [!Note]  
> Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

O elemento **ServiceTask3** representa o terceiro painel de tarefas da loja online.

``` syntax
<ServiceTask3
    URL = "URL"
/>
```

## <a name="attributes"></a>Atributos



| Termo                                                                                                                             | Descrição                                                        |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span id="URL__required_"></span><span id="url__required_"></span><span id="URL__REQUIRED_"></span>**URL** (obrigatório)<br/> | URL da página da web que Windows Media Player exibe.<br/> |



 

## <a name="parentchild-elements"></a>Elementos pai/filho



| Hierarquia       | Elemento                       |
|-----------------|-------------------------------|
| Elementos pai | **ServiceInfo**               |
| Elementos filho  | **ButtonText**, **ButtonTip** |



 

## <a name="remarks"></a>Comentários

**ServiceTask1** é considerado o painel de tarefas principal para envolvimento em atividades comerciais. É o painel de tarefas exibido quando o usuário escolhe comprar música. Use **ServiceTask3** para outra atividade de loja online.

> [!Note]  
> o Windows Media Player 10 tem três painéis de tarefas em que um repositório online pode exibir suas páginas da web. O repositório online pode optar por usar um, dois ou todos os três painéis de tarefas. o Windows Media Player 11 tem apenas um painel de tarefas, que pode ser exibido pelo usuário clicando na guia **lojas Online** . Windows Media Player 11 ignora os elementos **ServiceTask2** e **ServiceTask3** .

 

Os painéis de tarefas de lojas online compartilham uma única instância do navegador. Isso significa que você não deve escrever o código de script em sua página da Web que você espera que continue a ser executado quando o usuário mudar para a tarefa de serviço atual.

quando o usuário alterna os painéis de tarefas, Windows Media Player armazena a URL e os cookies de sessão. Quando o usuário volta ao painel de tarefas, o Player restaura a URL e os cookies. Se o usuário optar por usar uma loja online diferente, os dados da URL e da sessão serão apagados.

A tabela a seguir detalha os parâmetros enviados com a solicitação de URL.



| Nome         | Valor                                                                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *GeoId*      | ID de localização geográfica Windows. A ID de local é especificada pelo usuário na área **local** das configurações de opções regionais e de idiomas no painel de controle. |
| *locale*     | ID de localidade Windows Media Player.                                                                                                                                     |
| *UserLocale* | ID de localidade Windows. A localidade é especificada pelo usuário na área **padrões e formatos** das configurações de opções regionais e de idiomas no painel de controle.        |
| *version*    | Windows Media Player número de versão usando o seguinte formato: 10.0. x. xxxx ou 11.0. x. xxxx.                                                                         |



 

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

 

 





