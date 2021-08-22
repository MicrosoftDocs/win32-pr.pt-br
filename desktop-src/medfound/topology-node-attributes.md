---
description: Atributos de nó de topologia
ms.assetid: 584c0670-9051-4d03-9635-c8fadc8798c3
title: Atributos de nó de topologia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2ffd366c03607c4fc6646a09dae8571e6e4847a45b985f4996d28c15a828937
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034664"
---
# <a name="topology-node-attributes"></a>Atributos de nó de topologia

Os atributos a seguir se aplicam a nós de topologia.

## <a name="general-topology-node-attributes"></a>Atributos de nó de topologia geral



| Atributo                                                                       | Descrição                                                                                                                                              |
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_método de \_ conexão MF TOPONODE \_**](mf-toponode-connect-method-attribute.md)   | Especifica como o carregador de topologia conecta esse nó de topologia e se esse nó é opcional.                                                        |
| [**\_decodificador MF TOPONODE \_**](mf-toponode-decoder-attribute.md)                  | Especifica se o objeto de um nó topologia é um decodificador.                                                                                                  |
| [**\_descriptografador TOPONODE MF \_**](mf-toponode-decryptor-attribute.md)              | Especifica se um objeto subjacente do nó topologia é um descriptografador.                                                                                     |
| [**\_TOPONODE MF \_ Descartado**](mf-toponode-discardable-attribute.md)          | Especifica se o pipeline pode descartar amostras de um nó de topologia.                                                                                    |
| [**\_TOPONODE de \_ erro \_ MF**](mf-toponode-error-majortype-attribute.md) | Contém o tipo de mídia principal para um nó de topologia. Esse atributo é definido quando a topologia não é carregada porque não foi possível encontrar o decodificador correto. |
| [**subtipo de \_ erro MF TOPONODE \_ \_**](mf-toponode-error-subtype-attribute.md)     | Contém o subtipo de mídia para um nó de topologia. Esse atributo é definido quando a topologia não é carregada porque não foi possível encontrar o decodificador correto.    |
| [**\_código de TOPONODE MF \_**](mf-toponode-errorcode-attribute.md)              | Contém o código de erro da falha de conexão mais recente para esse nó de topologia.                                                                  |
| [**\_TOPONODE MF \_ bloqueado**](mf-toponode-locked-attribute.md)                    | Especifica se os tipos de mídia podem ser alterados neste nó de topologia.                                                                                  |
| [**\_Mark TOPONODE do MF \_ \_ aqui**](mf-toponode-markin-here-attribute.md)         | Especifica se o pipeline aplica o marca-in neste nó.                                                                                             |
| [**\_marcação de TOPONODE MF \_ \_ aqui**](mf-toponode-markout-here-attribute.md)       | Especifica se o pipeline aplica a marcação neste nó.                                                                                            |



 

## <a name="source-node-attributes"></a>Atributos do nó de origem



| Atributo                                                                                       | Descrição                                                                                                       |
|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [**\_TOPONODE MF \_ MEDIASTART**](mf-toponode-mediastart-attribute.md)                            | Especifica a hora de início de uma apresentação, em relação ao início do arquivo de origem de mídia, em unidades de 100 a nanossegundos. |
| [**\_TOPONODE MF \_ MEDIASTOP**](mf-toponode-mediastop-attribute.md)                              | Especifica a hora de parada de uma apresentação, em relação ao início do arquivo de origem de mídia, em unidades de 100 a nanossegundos.  |
| [**\_ \_ descritor de apresentação do MF TOPONODE \_**](mf-toponode-presentation-descriptor-attribute.md) | Contém um ponteiro para o descritor de apresentação para a origem da mídia.                                           |
| [**\_elemento de \_ sequência \_ TOPONODE MF**](mf-toponode-sequence-elementid-attribute.md)           | Especifica o elemento que contém um nó de origem.                                                                |
| [**\_origem MF TOPONODE \_**](mf-toponode-source-attribute.md)                                    | Contém um ponteiro para a fonte de mídia associada a um nó de topologia.                                           |
| [**\_ \_ descritor de fluxo de TOPONODE MF \_**](mf-toponode-stream-descriptor-attribute.md)             | Contém um ponteiro para o descritor de fluxo para a origem da mídia.                                                 |
| [**\_ID da \_ fila de TOPONODE MF \_**](mf-toponode-workqueue-id-attribute.md)                       | Especifica uma fila de trabalho para um nó de topologia.                                                                       |
| [**\_classe TOPONODE do MF \_ fila do \_ MMCSS \_**](mf-toponode-workqueue-mmcss-class-attribute.md)    | Especifica uma tarefa do serviço de Agendador de classes de multimídia (MMCSS) para um nó de topologia.                                  |
| [**\_TaskId TOPONODE \_ fila \_ de \_ tarefas do MMCSS**](mf-toponode-workqueue-mmcss-taskid-attribute.md)  | Especifica um identificador de tarefa do MMCSS para um nó de topologia.                                                            |



 

## <a name="transform-node-attributes"></a>Atributos de nó de transformação



| Atributo                                                                             | Descrição                                                                                                |
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**\_TOPONODE MF \_ D3DAWARE**](mf-toponode-d3daware-attribute.md)                      | Especifica se a transformação associada a um nó de topologia dá suporte a DXVA (aceleração de vídeo do DirectX) |
| [**\_dreno TOPONODE de MF \_**](mf-toponode-drain-attribute.md)                            | Especifica quando uma transformação é descarregada.                                                                     |
| [**\_liberação de TOPONODE MF \_**](mf-toponode-flush-attribute.md)                            | Especifica quando uma transformação é liberada.                                                                     |
| [**\_OBJECTID de \_ transformação \_ TOPONODE MF**](mf-toponode-transform-objectid-attribute.md) | O identificador de classe (CLSID) da transformação associada a este nó de topologia.                          |



 

## <a name="output-node-attributes"></a>Atributos do nó de saída



| Atributo                                                                                  | Descrição                                                                                                      |
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [**TOPONODE do MF \_ \_ desabilitar o \_ prelance**](mf-toponode-disable-preroll-attribute.md)            | Especifica se a sessão de mídia usa a preversão no coletor de mídia representado por esse nó de topologia.            |
| [**MF \_ TOPONODE \_ parashutdown \_ on \_ Remove**](mf-toponode-noshutdown-on-remove-attribute.md) | Especifica se a sessão de mídia desliga o coletor de mídia quando o nó de saída é removido da topologia. |
| [**MF \_ TOPONODE sem \_ taxa**](mf-toponode-rateless-attribute.md)                           | Especifica se o coletor de mídia associado a este nó de topologia é sem taxa.                                 |
| [**\_ \_ streamid TOPONODE MF**](mf-toponode-streamid-attribute.md)                           | O identificador de fluxo do coletor de fluxo associado a este nó de topologia.                                     |



 

## <a name="tee-node-attributes"></a>Atributos de nó de t



| Atributo                                                                  | Descrição                                                 |
|----------------------------------------------------------------------------|-------------------------------------------------------------|
| [**\_TOPONODE MF \_ PrimaryOutput porque**](mf-toponode-primaryoutput-attribute.md) | Indica qual saída é a saída primária em um nó de t. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Atributos de Media Foundation](media-foundation-attributes.md)
</dt> <dt>

[Atributos de topologia](topology-attributes.md)
</dt> </dl>

 

 



