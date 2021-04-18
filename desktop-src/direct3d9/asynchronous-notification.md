---
description: Há um número de consultas interessantes em um driver que um aplicativo pode fazer se não houver nenhum custo de desempenho.
ms.assetid: 81e1c5c5-03bc-4598-814e-14e56513e221
title: Notificação assíncrona (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8aee8acb791e2e1e2de7eb305cc19df4e7711e2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105771494"
---
# <a name="asynchronous-notification-direct3d-9"></a>Notificação assíncrona (Direct3D 9)

Há um número de consultas interessantes em um driver que um aplicativo pode fazer se não houver nenhum custo de desempenho. No Direct3D 7 e no Direct3D 8, um mecanismo de consulta síncrono, GetInfo, funcionou bem para coisas como estatísticas, mas nenhuma consulta de desempenho crítico foi adicionada. Há outras coisas (como limites) que são inerentemente assíncronas. Trata-se de uma API simples para fazer consultas síncronas. GetInfo será desativado no Direct3D 9.

Crie uma consulta usando [**IDirect3DDevice9:: CreateQuery**](/windows/desktop/api). Esse método usa um D3DQUERYTYPE, que define o tipo de consulta a ser feita e retorna um ponteiro para um objeto [**IDirect3DQuery9**](/windows/desktop/api) . Se não houver suporte para o tipo de consulta, a chamada retornará um erro D3DERR \_ não disponível. Usando o objeto Query, o aplicativo envia a consulta para o tempo de execução usando [**IDirect3DQuery9:: Issue**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue)e sonda o status da consulta usando [**IDirect3DQuery9:: GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata). Se o resultado da consulta estiver disponível, S \_ OK será retornado; caso contrário, \_ será retornado s false. Espera-se que o aplicativo passe um buffer de tamanho adequado para os resultados da consulta.

O aplicativo tem uma opção para forçar o tempo de execução para liberar a consulta para o driver usando D3DGETDATA \_ Flush com [**IDirect3DQuery9:: GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata). Isso causa uma liberação, forçando o driver a ver a consulta. Nesse caso, D3DERR \_ DEVICELOST será retornado se o dispositivo for perdido.

Todas as consultas são perdidas quando o dispositivo é perdido, o aplicativo precisa recriá-las. Se o dispositivo não oferecer suporte à consulta e o pQueryID for **nulo**, a criação da consulta falhará com D3DERR \_ INVALIDCALL.

A tabela a seguir resume informações importantes sobre cada tipo de consulta.



| QuertyType                    | Sinalizador de problema válido              | Buffer GetData              | Runtime      | Início implícito da consulta |
|-------------------------------|-------------------------------|-----------------------------|--------------|-----------------------------|
| D3DQUERYTYPE \_ VCACHE          | D3DISSUE \_ fim                 | D3DDEVINFO \_ VCACHE          | Varejo/depuração | CreateDevice                |
| \_RESOURCEMANAGER D3DQUERYTYPE | D3DISSUE \_ fim                 | \_RESOURCEMANAGER D3DDEVINFO | Somente depuração   | Presente                     |
| D3DQUERYTYPE \_ VERTEXSTATS     | D3DISSUE \_ fim                 | D3DDEVINFO \_ D3DVERTEXSTATS  | Somente depuração   | Presente                     |
| \_Evento D3DQUERYTYPE           | D3DISSUE \_ fim                 | BOOL                        | Varejo/depuração | CreateDevice                |
| D3DQUERYTYPE \_ oclusão       | Início do D3DISSUE \_ , \_ término do D3DISSUE | DWORD                       | Varejo/depuração | N/D                         |



 

Campo de sinalizadores para [**IDirect3DQuery9:: Issue**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue):


```
#define D3DISSUE_END (1 << 0) 
// Tells the runtime to issue the end of a query, changing its state to 
//   "non-signaled" 
```




```
 
#define D3DISSUE_BEGIN (1 << 1) // Tells the runtime to issue the 
// beginning of a query. 
```



Campo de sinalizadores para [**IDirect3DQuery9:: GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata):


```
 
#define D3DGETDATA_FLUSH (1 << 0) // Tells the runtime to flush 
// if the query is outstanding.
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Dicas de programação](programming-tips.md)
</dt> </dl>

 

 
