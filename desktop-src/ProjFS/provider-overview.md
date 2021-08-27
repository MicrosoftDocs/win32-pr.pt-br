---
title: Visão geral do provedor
description: Visão geral conceitual de um aplicativo de provedor.
ms.assetid: <GUID-GOES-HERE>
ms.date: 01/17/2020
ms.topic: article
ms.openlocfilehash: c6905d6d2d52fd30b8950682c45c9d3bd0fc13281fc0f1d3120cba1b168012d5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127956"
---
# <a name="provider-overview"></a>Visão geral do provedor

O provedor é um aplicativo de modo de usuário que mantém e compreende um armazenamento de dados de back-back.  O provedor implementa retornos de chamada ProjFS e usa a API do ProjFS para projetar esse armazenamento de dados no sistema de arquivos em que ele aparece para o usuário como arquivos e diretórios.  O armazenamento de backing do provedor pode ser local para o sistema do usuário ou pode estar localizado remotamente.

## <a name="data-projection"></a>Projeção de dados

A parte do sistema de arquivos que o provedor possui, em que seus dados são projetados, tem como raiz um diretório chamado "raiz de virtualização".  Quando o provedor deseja começar a projetar seus dados, ele inicia uma "instância de virtualização", que é um objeto que gerencia a comunicação entre o provedor e o ProjFS para o conjunto de arquivos e diretórios localizados em uma raiz de virtualização específica.  Todos os arquivos e diretórios descendentes da raiz de virtualização que não foram criados localmente pelo usuário são materializados pelo provedor por meio da API projFS.  Esses itens começam como arquivos virtuais e diretórios, o que significa que eles não existem no dispositivo de armazenamento local do usuário, mas são injetados nos resultados da enumeração pelo ProjFS.  À medida que os itens são abertos e lidos, o ProjFS invoca retornos de chamada implementados pelo provedor para solicitar dados e o provedor usa APIs do ProjFS para enviar esses dados para o armazenamento local em que eles são armazenados em cache para acesso subsequente.  Se a exibição do usuário do armazenamento de dados de back-back precisar ser alterada, por exemplo, se o conteúdo do armazenamento de dados tiver sido alterado, o provedor poderá usar APIs do ProjFS para atualizar ou excluir itens locais para refletir a nova exibição do armazenamento de dados.

## <a name="callback-return-codes"></a>Códigos de retorno de chamada

Cada retorno de chamada lista vários valores de retorno possíveis específicos para esse retorno de chamada.  Além dos valores de retorno listados para um retorno de chamada determinado, um retorno de chamada também pode retornar determinados outros códigos de erro.  Esta é a lista completa de códigos de erro que um retorno de chamada pode retornar:

| Código do Erro                                    | Significado
|-----------------------------------------------|--------
| S_OK                                          | Operação bem-sucedida
| E_OUTOFMEMORY                                 | Falha ao alocar a memória necessária.
| HRESULT_FROM_WIN32(ERROR_IO_PENDING)          | O provedor deseja concluir a operação posteriormente.
| HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER) | Um buffer passado para um retorno de chamada era muito pequeno.
| HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND)      | O arquivo não existe no armazenamento de back-back do provedor.
| HRESULT_FROM_WIN32(ERROR_INVALID_PARAMETER)   | Um argumento de retorno de chamada é inválido.  Por exemplo, uma ID de enumeração não corresponde a uma sessão de enumeração ativa.
| HRESULT_FROM_WIN32(ERROR_ACCESS_DENIED)       | O provedor deseja impedir que uma operação, como renomear ou excluir, seja realizada.

Os retornos de chamada também podem retornar erros que possam receber de chamadas para APIs do ProjFS.
Se um retorno de chamada retornar um código de erro que não está na lista anterior ou que não veio de uma API projFS, o ProjFS o retornará ao sistema de arquivos como STATUS_INTERNAL_ERROR.
