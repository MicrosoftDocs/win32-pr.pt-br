---
description: Um aplicativo deve ser capaz de produzir e consumir dados de vários formatos.
ms.assetid: bf60fab7-866b-4659-8316-653509ac5112
title: Formatos de persistência
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1853dc316d25395a30a15b02734ea4b7ed901b92379e04faa42f5abe5e768af5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119596636"
---
# <a name="persistence-formats"></a>Formatos de persistência

Um aplicativo deve ser capaz de produzir e consumir dados de vários formatos. Elas geralmente incluem formatos binários proprietários e também devem incluir alguns formatos padrão, como RTF (Rich Text Format) ou HTML.

A tabela a seguir lista alguns formatos que podem conter tinta.



| Formatar                                      | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Binário<br/>                           | Os aplicativos devem usar o formato serializado de tinta (ISF) para codificar tinta em seus formatos binários.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| HTML<br/>                             | Um formato HTML é altamente recomendado para a representação de conteúdo heterogêneo. Os aplicativos devem usar gif (Graphics Interchange Format) para codificar tinta em seus documentos HTML. Para obter mais informações sobre GIFs com segurança, consulte [Blocos de construção](building-blocks.md).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Imagem<br/>                            | Para aplicativos para os quais não há nenhuma outra interseção de compatibilidade, um aplicativo habilitado para tinta deve mover imagens formatadas de bitmap e metarquivo para a Área de Transferência.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| ISF (formato ISF)<br/>      | O ISF é a representação mais compacta e persistente de tinta. Embora geralmente contenha apenas dados de tinta, o ISF é extensível. Os aplicativos podem definir atributos personalizados (identificados por um GUID (identificador global exclusivo)) em um objeto [**Ink,**](inkdisp-class.md) traço de tinta ou ponto de tinta. Isso permite que você armazene qualquer tipo de dados ou metadados como um atributo em um fluxo ISF. Para interoperabilidade da Área de Transferência, a tinta pode ser colocada em um slot de Área de Transferência padrão para ISF definido nos arquivos de header do SDK (software development kit).<br/> O ISF é um formato específico da Tecnologia de Pc tablet [](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-load) da Microsoft e tem suporte apenas nos métodos [**Carregar**](inkdisp-class.md) e [**Salvar do**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-save) objeto Ink.<br/> |
| RTF<br/>                              | É possível gerar um formato de Área de Transferência RTF e codificar tinta no RTF como objetos OLE. Isso permite que a tinta seja colar em um contêiner OLE, como Microsoft Word ou um aplicativo baseado em RichEdit.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| {1&gt;linguagem XML&lt;1}<br/> | Os aplicativos podem usar qualquer um dos formatos de tinta codificados em base 64 para armazenar tinta em um formato de arquivo XML. Um formato XML é útil para inserir conteúdo de tinta em um banco de dados, como no caso de um campo de assinatura ou até mesmo como um formato de arquivo primário de aplicativos. Isso alivia a necessidade de escrever um analisador.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                        |



 

 

 




