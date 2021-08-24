---
title: Carregamento do IAgent
description: Carregamento do IAgent
ms.assetid: 8f25e6b6-a117-4b37-969a-d8f80c7be224
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae718ee8c6566de42645c5c02c2efada90ef85ba0136a112bcf0420d18a7b511
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119725386"
---
# <a name="iagentload"></a>IAgent::Load

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT Load(
   VARIANT vLoadKey,  // data provider
   long * pdwCharID,  // address of a variable for character ID
   long * pdwReqID    // address of a variable for request ID
);
```

Carrega um caractere na coleção [**Caracteres.**](./iagent.md)

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="vLoadKey"></span><span id="vloadkey"></span><span id="VLOADKEY"></span>*vLoadKey*
</dt> <dd>

Um tipo de dados variante que deve ser um dos seguintes:



| Valor           | Descrição                                                                      |
|------------|-----------------------------------------------------------------------|
| *Filespec* | O local do arquivo local do arquivo de definição do caractere especificado. |
| *URL*      | O endereço HTTP para o arquivo de definição do caractere.                 |



 

</dd> <dt>

<span id="pdwCharID"></span><span id="pdwcharid"></span><span id="PDWCHARID"></span>*pdwCharID*
</dt> <dd>

Endereço de uma variável que recebe a ID do caractere.

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

Endereço de uma variável que recebe a ID [**da**](load-method.md) solicitação de carregamento.

</dd> </dl>

Você pode carregar caracteres do subdiretório do Microsoft Agent especificando um caminho relativo (um que não inclui dois-pontos ou um caractere de barra à frente). Isso prefixa o caminho com o diretório de caracteres do Agent (localizado no diretório %windows% \\ msagent localizado). Você também pode usar um endereço relativo para especificar seu próprio diretório no diretório Chars do Agent.

Não é possível carregar o mesmo caractere (um caractere com o mesmo GUID) mais de uma vez de uma única conexão. Da mesma forma, você não pode carregar o caractere padrão e outros caracteres ao mesmo tempo de uma única conexão, porque o caractere padrão pode ser o mesmo que o outro caractere. No entanto, você pode criar outra conexão (usando CoCreateInstance) e carregar o mesmo caractere.

O provedor de dados do Microsoft Agent dá suporte ao carregamento de dados de caractere armazenados como um único arquivo estruturado (. ACS) com dados de caractere e dados de animação juntos ou como dados de caracteres separados (. ACF) e animação (. Arquivos ACA). Em geral, use o único estruturado. Arquivo ACS para carregar um caractere armazenado em uma unidade de disco local ou rede e acessado usando o protocolo de arquivo convencional (como nomes de caminho UNC). Use o separado. ACF e . Arquivos ACA quando você deseja carregar os arquivos de animação individualmente de um site remoto em que eles são acessados usando o protocolo HTTP.

Para. Arquivos ACS, usando o [**método Load,**](load-method.md) fornece acesso às animações de um caractere; depois de carregado, você pode usar o [**método Play**](play-method.md) para animar o caractere. Para. Arquivos ACF, você também usa o método [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) para carregar dados de animação. O **método Load** não dá suporte ao download de . Arquivos ACS de um site HTTP.

Carregar um caractere não exibe automaticamente o caractere. Use o [**método Show**](show-method.md) primeiro para tornar o caractere visível.

 

 