---
title: Visão geral do provedor
description: Visão geral conceitual de um aplicativo de provedor.
ms.assetid: <GUID-GOES-HERE>
ms.date: 01/17/2020
ms.topic: article
ms.openlocfilehash: 89b49096b7b68a723b52b4eb998c446661b7d3c9
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104454507"
---
# <a name="provider-overview"></a>Visão geral do provedor

O provedor é um aplicativo de modo de usuário que mantém e compreende um armazenamento de dados de backup.  O provedor implementa retornos de chamada ProjFS e usa a API ProjFS para projetar esse armazenamento de dados no sistema de arquivos onde ele aparece para o usuário como arquivos e diretórios.  O repositório de backup do provedor pode ser local para o sistema do usuário ou pode estar localizado remotamente.

## <a name="data-projection"></a>Projeção de dados

A parte do sistema de arquivos que o provedor possui, em que seus dados são projetados, tem raiz em um diretório chamado "raiz de virtualização".  Quando o provedor quer começar a projetar seus dados, ele inicia uma "instância de virtualização", que é um objeto que gerencia a comunicação entre o provedor e o ProjFS para o conjunto de arquivos e diretórios localizados em uma raiz de virtualização específica.  Todos os arquivos e diretórios que são descendentes da raiz de virtualização que não foram criados localmente pelo usuário são materializados pelo provedor por meio da API ProjFS.  Esses itens começam como arquivos e diretórios virtuais, o que significa que eles não existem no dispositivo de armazenamento local do usuário, mas são injetados em resultados de enumeração por ProjFS.  À medida que os itens são abertos e lidos, o ProjFS invoca os retornos de chamada implementados pelo provedor para solicitar dados, e o provedor usa APIs ProjFS para enviar esses dados para o armazenamento local onde ele é armazenado em cache para acesso subsequente.  Se o modo de exibição do usuário do armazenamento de dados de backup precisar ser alterado, por exemplo, se o conteúdo do armazenamento de dados tiver sido alterado, o provedor poderá usar APIs ProjFS para atualizar ou excluir itens locais para refletir a nova exibição do armazenamento de dados.

## <a name="callback-return-codes"></a>Códigos de retorno de retorno de chamada

Cada retorno de chamada lista vários valores de retorno possíveis específicos para esse retorno de chamada.  Além dos valores de retorno listados para um determinado retorno de chamada, um retorno de chamada também pode retornar alguns outros códigos de erro.  Esta é a lista completa de códigos de erro que um retorno de chamada pode retornar:

| Código do Erro                                    | Significado
|-----------------------------------------------|--------
| S_OK                                          | Operação bem-sucedida
| E_OUTOFMEMORY                                 | Falha ao alocar a memória necessária.
| HRESULT_FROM_WIN32 (ERROR_IO_PENDING)          | O provedor deseja concluir a operação em um momento posterior.
| HRESULT_FROM_WIN32 (ERROR_INSUFFICIENT_BUFFER) | Um buffer passado para um retorno de chamada era muito pequeno.
| HRESULT_FROM_WIN32 (ERROR_FILE_NOT_FOUND)      | O arquivo não existe no repositório de backup do provedor.
| HRESULT_FROM_WIN32 (ERROR_INVALID_PARAMETER)   | Um argumento de retorno de chamada é inválido.  Por exemplo, uma ID de enumeração não corresponde a uma sessão de enumeração ativa.
| HRESULT_FROM_WIN32 (ERROR_ACCESS_DENIED)       | O provedor deseja impedir que uma operação, como renomear ou excluir, ocorra.

Os retornos de chamada também podem retornar quaisquer erros que possam receber de chamadas para APIs ProjFS.
Se um retorno de chamada retornar um código de erro que não está na lista anterior ou que não foi proveniente de uma API ProjFS, ProjFS retornará ao sistema de arquivos como STATUS_INTERNAL_ERROR.
