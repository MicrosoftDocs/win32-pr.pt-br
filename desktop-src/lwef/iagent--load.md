---
title: IAgent carga
description: IAgent carga
ms.assetid: 8f25e6b6-a117-4b37-969a-d8f80c7be224
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4e30a25abb631714384f8349a9d260deade0d6d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103917282"
---
# <a name="iagentload"></a>IAgent:: Load

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT Load(
   VARIANT vLoadKey,  // data provider
   long * pdwCharID,  // address of a variable for character ID
   long * pdwReqID    // address of a variable for request ID
);
```

Carrega um caractere na coleção de [**caracteres**](./iagent.md) .

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="vLoadKey"></span><span id="vloadkey"></span><span id="VLOADKEY"></span>*vLoadKey*
</dt> <dd>

Um tipo de dados Variant que deve ser um dos seguintes:



|            |                                                                       |
|------------|-----------------------------------------------------------------------|
| *filespec* | O local do arquivo local do arquivo de definição do caractere especificado. |
| *URL*      | O endereço HTTP para o arquivo de definição do caractere.                 |



 

</dd> <dt>

<span id="pdwCharID"></span><span id="pdwcharid"></span><span id="PDWCHARID"></span>*pdwCharID*
</dt> <dd>

Endereço de uma variável que recebe a ID do caractere.

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

Endereço de uma variável que recebe a ID da solicitação de [**carregamento**](load-method.md) .

</dd> </dl>

Você pode carregar caracteres do subdiretório do Microsoft Agent especificando um caminho relativo (um que não inclua dois pontos ou um caractere de barra à esquerda). Isso prefixa o caminho com o diretório de caracteres do agente (localizado no diretório% Windows% \\ MSAgent localizado). Você também pode usar um endereço relativo para especificar seu próprio diretório no diretório de caracteres do agente.

Não é possível carregar o mesmo caractere (um caractere com o mesmo GUID) mais de uma vez a partir de uma única conexão. Da mesma forma, você não pode carregar o caractere padrão e outros caracteres ao mesmo tempo de uma única conexão, porque o caractere padrão pode ser o mesmo que o outro caractere. No entanto, você pode criar outra conexão (usando CoCreateInstance) e carregar o mesmo caractere.

O provedor de dados do Microsoft Agent dá suporte ao carregamento de dados de caracteres armazenados como um único arquivo estruturado (. ACS) com dados de caractere e dados de animação juntos, ou como dados de caractere separados (. ACF) e animação (. ACA) arquivos. Em geral, use a estrutura única. Arquivo ACS para carregar um caractere que é armazenado em uma unidade de disco ou rede local e acessado usando o protocolo de arquivo convencional (como caminhos UNC). Use a separada. ACF e. ACA arquivos quando você deseja carregar os arquivos de animação individualmente de um site remoto onde eles são acessados usando o protocolo HTTP.

Fins. Os arquivos ACS, usando o método [**Load**](load-method.md) , fornecem acesso às animações de um caractere; Depois de carregado, você pode usar o método [**Play**](play-method.md) para animar o caractere. Fins. Arquivos ACF, você também usa o método [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) para carregar dados de animação. O método **Load** não oferece suporte ao download. Arquivos ACS de um site HTTP.

O carregamento de um caractere não exibe automaticamente o caractere. Use o método [**show**](show-method.md) primeiro para tornar o caractere visível.

 

 