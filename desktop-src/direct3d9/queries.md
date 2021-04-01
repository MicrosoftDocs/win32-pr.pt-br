---
description: Há vários tipos de consultas que são projetadas para consultar o status dos recursos.
ms.assetid: 2c65d199-141d-43a7-b513-4cb4459d7c27
title: Consultas (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22f450aa7015d4b66ad28b6c4d0632b2995bedd7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825488"
---
# <a name="queries-direct3d-9"></a>Consultas (Direct3D 9)

Há vários tipos de consultas que são projetadas para consultar o status dos recursos. O status de um determinado recurso inclui o status da GPU (unidade de processamento gráfico), o status do driver ou o status do tempo de execução. Para entender a diferença entre os diferentes tipos de consulta, você precisa entender os Estados de consulta. O diagrama de transição de estado a seguir explica cada um dos Estados de consulta.

![diagrama mostrando transições entre Estados de consulta](images/queries.png)

O diagrama mostra três Estados, cada um definido pelos círculos. Cada uma das linhas sólidas são eventos controlados por aplicativo que causam uma transição de estado. A linha tracejada é um evento controlado por recursos que alterna uma consulta do estado emitido para o estado sinalizado. Cada um desses Estados tem uma finalidade diferente:

-   O estado sinalizado é como um estado ocioso. O objeto de consulta foi gerado e está aguardando que o aplicativo emita a consulta. Depois que uma consulta for concluída e feita a transição de volta para o estado sinalizado, a resposta para a consulta poderá ser recuperada.
-   O estado de compilação é como uma área de preparo para uma consulta. A partir do estado de compilação, uma consulta foi emitida (chamando [**D3DISSUE \_ begin**](d3dissue-begin.md)), mas ainda não foi transferida para o estado emitido. Quando um aplicativo emite uma extremidade de consulta (chamando [**D3DISSUE \_ end**](d3dissue-end.md)), a consulta faz a transição para o estado emitido.
-   O estado emitido significa que o recurso que está sendo consultado tem controle da consulta. Depois que o recurso concluir seu trabalho, o recurso faz a transição da máquina de estado para o estado sinalizado. Durante o estado emitido, o aplicativo deve sondar para detectar a transição para o estado sinalizado. Quando ocorre a transição para o estado sinalizado, [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) retorna o resultado da consulta (por meio de um argumento) para o aplicativo.

A tabela a seguir lista os tipos de consulta disponíveis.



| Tipo de consulta        | Evento de problema                                                                      | Buffer GetData                                                              | Runtime      | Início implícito da consulta                      |
|-------------------|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------|--------------|--------------------------------------------------|
| BANDWIDTHTIMINGS  | [**D3DISSUE \_ Início**](d3dissue-begin.md), [ **\_ fim do D3DISSUE**](d3dissue-end.md) | [**D3DDEVINFO \_ D3D9BANDWIDTHTIMINGS**](d3ddevinfo-d3d9bandwidthtimings.md) | Varejo/depuração | N/D                                              |
| CACHEUTILIZATION  | [**D3DISSUE \_ Início**](d3dissue-begin.md), [ **\_ fim do D3DISSUE**](d3dissue-end.md) | [**D3DDEVINFO \_ D3D9CACHEUTILIZATION**](d3ddevinfo-d3d9cacheutilization.md) | Varejo/depuração | N/D                                              |
| CIRCUNSTÂNCIA             | [**D3DISSUE \_ fim**](d3dissue-end.md)                                            | BOOL                                                                        | Varejo/depuração | [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) |
| INTERFACETIMINGS  | [**D3DISSUE \_ Início**](d3dissue-begin.md), [ **\_ fim do D3DISSUE**](d3dissue-end.md) | [**D3DDEVINFO \_ D3D9INTERFACETIMINGS**](d3ddevinfo-d3d9interfacetimings.md) | Varejo/depuração | N/D                                              |
| OCLUSÃO         | [**D3DISSUE \_ Início**](d3dissue-begin.md), [ **\_ fim do D3DISSUE**](d3dissue-end.md) | DWORD                                                                       | Varejo/depuração | N/D                                              |
| PIPELINETIMINGS   | [**D3DISSUE \_ Início**](d3dissue-begin.md), [ **\_ fim do D3DISSUE**](d3dissue-end.md) | [**D3DDEVINFO \_ D3D9PIPELINETIMINGS**](d3ddevinfo-d3d9pipelinetimings.md)   | Varejo/depuração | N/D                                              |
| RESOURCEMANAGER   | [**D3DISSUE \_ fim**](d3dissue-end.md)                                            | [**\_RESOURCEMANAGER D3DDEVINFO**](d3ddevinfo-resourcemanager.md)           | Somente depuração   | [**Existi**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)     |
| timestamp         | [**D3DISSUE \_ fim**](d3dissue-end.md)                                            | UINT64                                                                      | Varejo/depuração | N/D                                              |
| TIMESTAMPDISJOINT | [**D3DISSUE \_ Início**](d3dissue-begin.md), [ **\_ fim do D3DISSUE**](d3dissue-end.md) | BOOL                                                                        | Varejo/depuração | N/D                                              |
| TIMESTAMPFREQ     | [**D3DISSUE \_ fim**](d3dissue-end.md)                                            | UINT64                                                                      | Varejo/depuração | N/D                                              |
| VCACHE            | [**D3DISSUE \_ fim**](d3dissue-end.md)                                            | [**D3DDEVINFO \_ VCACHE**](d3ddevinfo-vcache.md)                             | Varejo/depuração | [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) |
| VERTEXSTATS       | [**D3DISSUE \_ fim**](d3dissue-end.md)                                            | [**D3DDEVINFO \_ D3DVERTEXSTATS**](d3ddevinfo-d3dvertexstats.md)             | Somente depuração   | [**Existi**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)     |
| VERTEXTIMINGS     | [**D3DISSUE \_ Início**](d3dissue-begin.md), [ **\_ fim do D3DISSUE**](d3dissue-end.md) | [**D3DDEVINFO \_ D3D9STAGETIMINGS**](d3ddevinfo-d3d9stagetimings.md)         | Varejo/depuração | N/D                                              |



 

Algumas das consultas exigem um evento de início e término, enquanto outras exigem apenas um evento de término. As consultas que exigem apenas um evento de término começam quando outro evento implícito ocorre (que é listado na tabela). Todas as consultas retornam uma resposta, exceto a consulta de evento cuja resposta é sempre **verdadeira**. Um aplicativo usa o estado da consulta ou o código de retorno de [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata).

## <a name="create-a-query"></a>Criar uma consulta

Antes de criar uma consulta, você pode verificar se o tempo de execução dá suporte a consultas chamando [**CreateQuery**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createquery) com um ponteiro **nulo** como este:


```
IDirect3DQuery9* pEventQuery;

// Create a device pointer m_pd3dDevice

// Create a query object
HRESULT hr = m_pd3dDevice->CreateQuery(D3DQUERYTYPE_EVENT, NULL);
```



Esse método retornará um código de êxito se uma consulta puder ser criada; caso contrário, ele retorna um código de erro. Depois que o [**CreateQuery**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createquery) for executado com sucesso, você poderá criar um objeto de consulta como este:


```
IDirect3DQuery9* pEventQuery;
m_pd3dDevice->CreateQuery(D3DQUERYTYPE_EVENT, &pEventQuery);
```



Se essa chamada for realizada com sucesso, um objeto de consulta será criado. A consulta está essencialmente ociosa no estado sinalizado (com uma resposta não inicializada) aguardando para ser emitida. Quando terminar com a consulta, libere-a como qualquer outra interface.

## <a name="issue-a-query"></a>Emitir uma consulta

Um aplicativo altera um estado de consulta emitindo uma consulta. Aqui está um exemplo de como emitir uma consulta:


```
IDirect3DQuery9* pEventQuery;
m_pD3DDevice->CreateQuery(D3DQUERYTYPE_EVENT, &pEventQuery);

// Issue a Begin event
pEventQuery->Issue(D3DISSUE_BEGIN);

or

// Issue an End event
pEventQuery->Issue(D3DISSUE_END);
```



Uma consulta no estado sinalizado fará a transição como esta quando for emitida:



| Tipo de problema                                | A consulta faz a transição para o. . . |
|-------------------------------------------|--------------------------------|
| [**Início do D3DISSUE \_**](d3dissue-begin.md) | Estado de compilação.                |
| [**D3DISSUE \_ fim**](d3dissue-end.md)     | Estado emitido.                  |



 

Uma consulta no estado de compilação será transferida como esta quando for emitida:



| Tipo de problema                                | A consulta faz a transição para o. . .                                            |
|-------------------------------------------|---------------------------------------------------------------------------|
| [**Início do D3DISSUE \_**](d3dissue-begin.md) | (Sem transição, permanece no estado de compilação. Reinicia o colchete de consulta.) |
| [**D3DISSUE \_ fim**](d3dissue-end.md)     | Estado emitido.                                                             |



 

Uma consulta no estado emitido fará a transição como esta quando for emitida:



| Tipo de problema                                | A consulta faz a transição para o. . .                    |
|-------------------------------------------|---------------------------------------------------|
| [**Início do D3DISSUE \_**](d3dissue-begin.md) | Criando o estado e reinicia o colchete de consulta.    |
| [**D3DISSUE \_ fim**](d3dissue-end.md)     | Estado emitido após abandonar a consulta existente. |



 

## <a name="check-the-query-state-and-get-the-answer-to-the-query"></a>Verificar o estado da consulta e obter a resposta para a consulta

[**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) faz duas coisas:

1.  Retorna o estado da consulta no código de retorno.
2.  Retorna a resposta à consulta em *pData*.

De cada um dos três Estados de consulta, aqui estão os códigos de retorno de [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) :



| Estado de consulta | Código de retorno GetData |
|-------------|---------------------|
| Sinalizado    | S \_ OK               |
| Construção    | Código do erro          |
| Emitido      | \_falso            |



 

Por exemplo, quando uma consulta está no estado emitido e a resposta à consulta não está disponível, [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) retorna S \_ false. Quando o recurso conclui seu trabalho e o aplicativo emitiu uma extremidade de consulta, o recurso faz a transição da consulta para o estado sinalizado. Do estado sinalizado, **GetData** retorna S \_ OK, o que significa que a resposta para a consulta também é retornada em *pData*. Por exemplo, aqui está a sequência de eventos para retornar o número de pixels desenhados em uma sequência de renderização:

-   Criar a consulta.
-   Emitir um evento de início.
-   Desenhe algo.
-   Emita um evento de término.

A seguir está a sequência de código correspondente:


```
IDirect3DQuery9* pOcclusionQuery;
DWORD numberOfPixelsDrawn;

m_pD3DDevice->CreateQuery(D3DQUERYTYPE_OCCLUSION, &pOcclusionQuery);

// Add an end marker to the command buffer queue.
pOcclusionQuery->Issue(D3DISSUE_BEGIN);

// API render loop
...
Draw(...)
...

// Add an end marker to the command buffer queue.
pOcclusionQuery->Issue(D3DISSUE_END);

// Force the driver to execute the commands from the command buffer.
// Empty the command buffer and wait until the GPU is idle.
while(S_FALSE == pOcclusionQuery->GetData( &numberOfPixelsDrawn, 
                                  sizeof(DWORD), D3DGETDATA_FLUSH ))
    ;
```



Essas linhas de código fazem várias coisas:

-   Chame [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) para retornar o número de pixels desenhados.
-   Especifique [**a \_ liberação de D3DGETDATA**](d3dgetdata-flush.md) para habilitar o recurso para fazer a transição da consulta para o estado sinalizado.
-   Sondar o recurso de consulta chamando [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) a partir de um loop. Desde que **GetData** retorne S \_ false, isso significa que o recurso ainda não retornou a resposta.

O valor de retorno de [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) essencialmente informa em que estado a consulta é. Os valores possíveis são S \_ OK, s \_ false e um erro. Não chame **GetData** em uma consulta que esteja no estado de compilação.

-   S \_ OK significa que o recurso (GPU ou driver ou tempo de execução) foi concluído. A consulta está retornando ao estado sinalizado. A resposta (se houver) está sendo retornada por [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata).
-   S \_ false significa que o recurso (GPU ou driver ou tempo de execução) não pode retornar uma resposta ainda. Isso pode ocorrer porque a GPU não foi concluída ou ainda não viu o trabalho.
-   Um erro significa que a consulta gerou um erro do qual não pode se recuperar. Esse pode ser o caso se o dispositivo for perdido durante uma consulta. Depois que uma consulta gerar um erro (diferente de S \_ false), a consulta deverá ser recriada, o que reiniciará a sequência de consulta do estado sinalizado.

Em vez de especificar [**D3DGETDATA \_ flush**](d3dgetdata-flush.md), que fornece informações mais atualizadas, você pode fornecer zero, que é uma verificação de peso mais leve se a consulta estiver no estado emitido. Fornecer zero fará com que [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) não libere o buffer de comando. Por esse motivo, deve-se ter cuidado para evitar loops infinate (consulte **GetData** para obter detalhes). Como o tempo de execução faz a fila funcionar no buffer de comando, o **D3DGETDATA \_ flush** é um mecanismo para liberar o buffer de comando para o driver (e, portanto, a GPU; consulte com [precisão a criação de perfil de chamadas de API do Direct3D (Direct3D 9)](accurately-profiling-direct3d-api-calls.md)). Durante a liberação do buffer de comando, uma consulta pode fazer a transição para o estado sinalizado.

## <a name="example-an-event-query"></a>Exemplo: uma consulta de evento

Uma consulta de evento não dá suporte a um evento de início.

-   Criar a consulta.
-   Emita um evento de término.
-   Sondagem até que a GPU esteja ociosa.
-   Emita um evento de término.


```
IDirect3DQuery9* pEventQuery = NULL;
m_pD3DDevice->CreateQuery(D3DQUERYTYPE_EVENT, &pEventQuery);

// Add an end marker to the command buffer queue.
pEventQuery->Issue(D3DISSUE_END);

// Empty the command buffer and wait until the GPU is idle.
while(S_FALSE == pEventQuery->GetData( NULL, 0, D3DGETDATA_FLUSH ))
    ;

... // API calls

// Add an end marker to the command buffer queue.
pEventQuery->Issue(D3DISSUE_END);

// Force the driver to execute the commands from the command buffer.
// Empty the command buffer and wait until the GPU is idle.
while(S_FALSE == pEventQuery->GetData( NULL, 0, D3DGETDATA_FLUSH ))
    ;
```



Essa é a sequência de comandos usada por uma consulta de evento para criar o perfil de chamadas de API (interface de programação de aplicativo) (consulte com [precisão a criação de perfis do Direct3D API (Direct3D 9)](accurately-profiling-direct3d-api-calls.md)). Essa sequência usa marcadores para ajudar a controlar a quantidade de trabalho no buffer de comando.

Observe que os aplicativos devem prestar atenção especial ao grande custo associado à liberação do buffer de comando, pois isso faz com que o sistema operacional mude para o modo kernel, o que incorrerá em uma penalidade de desempenho considerável. Os aplicativos também devem estar cientes do desperdício de ciclos de CPU aguardando a conclusão das consultas.

As consultas são uma otimização a ser usada durante a renderização para aumentar o desempenho. Portanto, não é benéfico gastar tempo aguardando a conclusão de uma consulta. Se uma consulta for emitida e se os resultados ainda não estiverem prontos no momento em que o aplicativo verificá-los, a tentativa de otimização não teve sucesso e a renderização deve continuar normalmente.

O exemplo clássico disso é durante a remoção de oclusão. Em vez do loop **while** acima, um aplicativo que usa consultas pode implementar a remoção de oclusão para verificar se uma consulta foi concluída no momento em que precisa do resultado. Se a consulta não tiver sido concluída, continue (como um cenário de pior caso) como se o objeto que está sendo testado não for obstruído (ou seja, visível) e renderizá-lo. O código deve ser semelhante ao seguinte.


```
IDirect3DQuery9* pOcclusionQuery = NULL;
m_pD3DDevice->CreateQuery( D3DQUERYTYPE_OCCLUSION, &pOcclusionQuery );

// Add a begin marker to the command buffer queue.
pOcclusionQuery->Issue( D3DISSUE_BEGIN );

... // API calls

// Add an end marker to the command buffer queue.
pOcclusionQuery->Issue( D3DISSUE_END );

// Avoid flushing and letting the CPU go idle by not using a while loop.
// Check if queries are finished:
DWORD dwOccluded = 0;
if( S_FALSE == pOcclusionQuery->GetData( &dwOccluded, sizeof(DWORD), 0 ) )
{
    // Query is not done yet or object not occluded; avoid flushing/wait by continuing with worst-case scenario
    pSomeComplexMesh->Render();
}
else if( dwOccluded != 0 )
{
    // Query is done and object is not occluded.
    pSomeComplexMesh->Render();
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tópicos avançados](advanced-topics.md)
</dt> </dl>

 

 
