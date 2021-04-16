---
title: Elemento MOREINFO
description: O elemento MOREINFO especifica uma URL para um site, endereço de email ou comando de script associado a um show, clip ou banner.
ms.assetid: b817ef1d-4ca0-45f4-942b-695eaf537110
keywords:
- Elemento MOREINFO do Windows Media Player
topic_type:
- apiref
api_name:
- MOREINFO Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: efc54fe9745566ec7eaa87b7f0f4645b07a055f0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105772970"
---
# <a name="moreinfo-element"></a>Elemento MOREINFO

O elemento **moreinfo** especifica uma URL para um site, endereço de email ou comando de script associado a um show, clip ou banner.

``` syntax
<MOREINFO
   HREF = "URL"
   TARGET = "Frame"
/>
```

## <a name="attributes"></a>Atributos

**Href** (obrigatório)

URL para um site, endereço de email ou comando de script.

**ALVO**

Valor que define o quadro ou a janela em que o navegador abrirá a página definida pelo atributo **href** .

Pode ser uma cadeia de caracteres que contém um nome de janela ou um dos valores a seguir.



| Valor    | Descrição                                                                                                              |
|----------|--------------------------------------------------------------------------------------------------------------------------|
| \_ficará  | O documento é carregado em uma nova janela do navegador.                                                                              |
| \_auto-restauração   | O documento é carregado no mesmo quadro que o documento atual que contém o controle do Windows Media Player.                |
| \_primária | O documento é carregado no quadro pai imediato do quadro atual ou no quadro atual, se não houver quadro pai. |
| \_Início    | O documento é carregado na janela completa do navegador, substituindo todos os outros quadros ou documentos.                                  |



 

## <a name="parentchild-elements"></a>Elementos pai/filho



| Hierarquia       | Elementos                       |
|-----------------|--------------------------------|
| Elementos pai | **ASX**, **entrada**, **faixa** |
| Elementos filho  | Nenhum                           |



 

## <a name="remarks"></a>Comentários

Esse elemento Especifica uma URL para um site, endereço de email **ou comando de script. O usuário pode acessar o destino da URL clicando no gráfico ou no texto associado** ao elemento moreinfo. Os detalhes dependem do elemento pai do elemento **moreinfo** :

-   Se o elemento **moreinfo** for o filho de um elemento **ASX** , o usuário poderá acessar a URL clicando no título mostrar.
-   Se o elemento **moreinfo** for o filho de um elemento de **entrada** , o usuário poderá acessar a URL clicando no título do clipe.
-   Se o elemento **moreinfo** for o filho de um elemento **banner** , o usuário poderá acessar a URL clicando no gráfico de faixa.

Se o atributo **href** especificar uma URL para um site, o navegador será aberto e navegará até a URL. Se o atributo **href** especificar um endereço de email, o aplicativo de email do usuário será iniciado. Se o atributo **href** especificar um comando de script, o comando de script será executado no navegador.

**Observação**

Se o elemento **moreinfo** aparecer dentro de um elemento **ASX** ou **entry** , quando o cursor do mouse for mantido sobre o título do show (para um elemento **ASX** ) ou um clip (para um elemento de **entrada** ), a URL definida no atributo **href** poderá ser selecionada e acessada pelo Windows Media Player.

O atributo de **destino** define o quadro ou a janela em que o navegador irá abrir a página definida pelo atributo **href** . Os valores para esse atributo seguem a sintaxe HTML padrão e as definições. No caso de um controle inserido em uma página da Web, se nenhum atributo de **destino** for definido, a URL carregará a janela atual do navegador e substituirá a página existente, o que significa que o conteúdo parará de ser reproduzido. Portanto, é recomendável que você sempre especifique um atributo de **destino** ao inserir o controle do Windows Media Player em uma página da Web.

Se o metarquivo é aberto no Windows Media Player autônomo, o atributo de **destino** é ignorado e a URL é carregada em uma janela de navegador existente. Se não houver janela do navegador aberta no momento, a URL será carregada em uma nova janela do navegador.

## <a name="examples"></a>Exemplos


```XML
<ASX VERSION="3.0">

   <TITLE>Example Media Player Show</TITLE>
   <MOREINFO HREF="https://example.microsoft.com/info/show_info.htm" />
   
   <ENTRY>
      <TITLE>Example Clip</TITLE>
      <MOREINFO HREF="https://example.microsoft.com/info/clip1_info.htm" />
      <REF HREF="mms://example.microsoft.com/media.asf" />
   </ENTRY>
   
</ASX>

```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------|
| Versão<br/> | Windows Media Player versão 70 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de elementos de metarquivo do Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Referência do metarquivo do Windows Media**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





