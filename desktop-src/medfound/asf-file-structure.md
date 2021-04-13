---
description: Este tópico descreve a estrutura de um arquivo ASF (Advanced Systems Format).
ms.assetid: 4a817efa-5452-46bf-8921-2ba199c21949
title: Estrutura de arquivo ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 672067b5f933884326038a93b6d4538c68558856
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501205"
---
# <a name="asf-file-structure"></a>Estrutura de arquivo ASF

Este tópico descreve a estrutura de um arquivo ASF (Advanced Systems Format).

Para obter informações detalhadas sobre arquivos ASF, baixe a [especificação do ASF](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea). Você também pode usar a ferramenta do [Windows Media ASF Viewer 9 Series](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea) para ver a estrutura de um arquivo ASF existente.

A unidade base da organização para arquivos ASF é chamada de *objeto*. Um objeto de arquivo ASF contém os dados a seguir.



| Dados                                                        | Tamanho     |
|-------------------------------------------------------------|----------|
| Um GUID que identifica o objeto.                          | 128 bits |
| O tamanho do objeto.                                     | 64 bits. |
| Dados do objeto. Os dados do objeto podem conter outros objetos ASF. | Varia.  |



 

> [!Note]  
> Um objeto de arquivo ASF é simplesmente uma parte dos dados. Não é um objeto no sentido de programação do computador.

 

Um arquivo ASF contém três tipos de objetos de arquivo de nível superior.



| Objeto de arquivo ASF                                                                                                                      | Descrição                                          |
|--------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span id="_Header_Object"></span><span id="_header_object"></span><span id="_HEADER_OBJECT"></span> Objeto de cabeçalho<br/>         | Contém informações sobre o arquivo ASF.<br/>  |
| <span id="Data_Object"></span><span id="data_object"></span><span id="DATA_OBJECT"></span>Objeto de dados<br/>                     | Contém pacotes de dados de mídia.<br/>           |
| <span id="_Index_Object_s_"></span><span id="_index_object_s_"></span><span id="_INDEX_OBJECT_S_"></span> Objeto (s) de índice<br/> | Contém um ou mais índices. (Opcional).<br/> |



 

O diagrama a seguir mostra a estrutura do arquivo ASF.

![diagrama mostrando a estrutura do arquivo ASF, incluindo itens dentro do cabeçalho, dos dados e do índice](images/asf-components04.png)

Este diagrama não é desenhado para escala; Normalmente, o objeto de dados compreende a maior parte do arquivo.

### <a name="header-object"></a>Objeto de cabeçalho

O objeto de cabeçalho é obrigatório e aparece no início de cada arquivo ASF. Ele contém atributos de arquivo globais e informações sobre os fluxos no arquivo ASF. Essas informações são usadas para interpretar e reproduzir os dados no arquivo.

O objeto de cabeçalho contém vários subobjetos madatory:

-   O objeto de propriedades de arquivo descreve os atributos globais do arquivo, como o tamanho do arquivo, a duração da reprodução, o número de pacotes de dados, o tamanho mínimo e máximo do pacote e a taxa de bits máxima.
-   O objeto de extensão de cabeçalho permite que a funcionalidade adicional seja adicionada a um arquivo ASF, mantendo a compatibilidade com versões anteriores.
-   O objeto de propriedades de fluxo descreve um fluxo no arquivo. Um arquivo ASF deve conter pelo menos um fluxo e, portanto, pelo menos um objeto de propriedades de fluxo.

O objeto de cabeçalho pode conter informações adicionais opcionais, incluindo metadados sobre o arquivo (como título e autor), uma lista dos codecs usados para codificar o arquivo e informações de proteção de conteúdo.

### <a name="data-object"></a>Objeto de dados

O objeto de dados ASF contém todos os dados de mídia para o arquivo ASF. Esse objeto é obrigatório e deve seguir o objeto de cabeçalho ASF.

O objeto de dados é dividido em *pacotes* de dados. Cada pacote contém dados para um ou vários fluxos no arquivo. Um pacote de dados contém um cabeçalho de pacote de dados que fornece informações de análise de pacote, seguidos pelos dados de carga dos dados de mídia digital reais. Todos os pacotes de dados têm um tempo de apresentação associado a ele e são organizados na ordem recebida.

As informações sobre o conteúdo do objeto de dados, como o tamanho do pacote e a contagem de pacotes, são armazenadas no objeto de cabeçalho.

### <a name="index-object"></a>Objeto de índice

O objeto de índice é opcional e é o último objeto no arquivo ASF. Um arquivo ASF pode conter mais de um objeto de índice. O objeto Index fornece acesso aleatório baseado em tempo ao objeto de dados ASF.

Um objeto de índice simples é outro tipo de índice.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Suporte a ASF no Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 




