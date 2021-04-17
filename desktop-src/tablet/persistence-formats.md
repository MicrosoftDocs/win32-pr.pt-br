---
description: Um aplicativo deve ser capaz de produzir e consumir dados de vários formatos.
ms.assetid: bf60fab7-866b-4659-8316-653509ac5112
title: Formatos de persistência
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a8edd88a4b170d2299832a205d80dc6704aea66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105813345"
---
# <a name="persistence-formats"></a>Formatos de persistência

Um aplicativo deve ser capaz de produzir e consumir dados de vários formatos. Elas geralmente incluem formatos binários proprietários e também devem incluir alguns formatos padrão, como Rich Text Format (RTF) ou HTML.

A tabela a seguir lista alguns formatos que podem conter tinta.



| Formatar                                      | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Binário<br/>                           | Os aplicativos devem usar o formato serializado da tinta (ISF) para codificar a tinta em seus formatos binários.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| HTML<br/>                             | Um formato HTML é altamente recomendado para a representação de conteúdo heterogêneo. Os aplicativos devem usar reforçada Graphics Interchange Format (GIF) para codificar a tinta em seus documentos HTML. Para obter mais informações sobre GIFs reforçada, consulte [blocos de construção](building-blocks.md).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Imagem<br/>                            | Para aplicativos para os quais não há nenhuma outra interseção de compatibilidade, um aplicativo habilitado para tinta deve mover imagens formatadas de bitmap e de metarquivo para a área de transferência.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| ISF (formato ISF)<br/>      | O ISF é a representação mais compacta e persistente de tinta. Embora geralmente contenha apenas dados de tinta, o ISF é extensível. Os aplicativos podem definir atributos personalizados (identificados por um identificador global exclusivo (GUID)) em um objeto de [**tinta**](inkdisp-class.md) , em um traço de tinta ou em um ponto de tinta. Isso permite que você armazene qualquer tipo de dados ou metadados como um atributo em um fluxo de ISF. Para a interoperabilidade da área de transferência, a tinta pode ser colocada em um slot de área de transferência padrão para ISF definido nos arquivos de cabeçalho do Software Development Kit (SDK).<br/> ISF é um formato específico para a tecnologia Microsoft Tablet PC e tem suporte apenas nos métodos [**Load**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-load) e [**Save**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-save) do objeto [**Ink**](inkdisp-class.md) .<br/> |
| RTF<br/>                              | É possível gerar um formato de área de transferência RTF e codificar a tinta no RTF como objetos OLE. Isso permite que a tinta seja colada em um contêiner OLE, como o Microsoft Word ou um aplicativo baseado em RichEdit.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| {1&gt;linguagem XML&lt;1}<br/> | Os aplicativos podem usar qualquer um dos formatos de tinta que são codificados em base 64 para armazenar a tinta em um formato de arquivo XML. Um formato XML é útil para inserir o conteúdo de tinta em um banco de dados, como no caso de um campo de assinatura, ou até mesmo como um formato de arquivo primário de aplicativos. Isso alivia a necessidade de escrever um analisador.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                        |



 

 

 




