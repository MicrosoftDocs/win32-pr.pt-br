---
description: Gerencie o compartilhamento de assembly e o controle de versão de DLL no armazenamento de assembly lado a lado dos programas. Escrever manifestos de assembly e descrever automaticamente os aplicativos para compartilhamento de assembly e redirecionamento de DLLs.
ms.assetid: 2f841eb6-9a6c-4c9b-b057-a3da6cd6b0b0
title: Aplicativos isolados e assemblies lado a lado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9af477178aa3fd68563ee53017d80c00e103b4cb97a6fd16062d307375b29574
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127486"
---
# <a name="isolated-applications-and-side-by-side-assemblies"></a>Aplicativos isolados e assemblies lado a lado

## <a name="purpose"></a>Finalidade

os aplicativos isolados e os Assemblies lado a lado são uma solução de Windows da Microsoft que reduz conflitos de controle de versão em aplicativos cliente Windows. com o Windows, os desenvolvedores de aplicativos podem criar aplicativos isolados totalmente autodescritivos e não afetados por alterações no registro, em outros aplicativos ou em outras versões de assemblies em execução no sistema. Os autores e administradores de aplicativos podem usar manifestos para gerenciar o compartilhamento de assemblies lado a lado após a implantação em uma base global ou por aplicativo. Os clientes se beneficiam de aplicativos isolados que são mais estáveis e mais confiáveis.

## <a name="where-applicable"></a>Quando aplicável

Os aplicativos isolados e o compartilhamento de assembly lado a lado podem ser usados para desenvolver aplicativos que compartilhem com segurança os assemblies do sistema operacional. Os desenvolvedores podem usar essa tecnologia para corrigir conflitos de versão de DLL causados por uma versão incompatível de um assembly compartilhado.

Se seu aplicativo precisar obter consistentemente a versão de um componente que você testou, é possível isolar seu aplicativo para que ele seja sempre executado com a versão testada do componente no computador do usuário.

Os aplicativos isolados e os assemblies lado a lado são destinados ao desenvolvimento de aplicativos de estilo de área de trabalho.

## <a name="developer-audience"></a>Público de desenvolvedores

Esta documentação destina-se principalmente a desenvolvedores de software, desenvolvedores de aplicativos e administradores de rede:

-   Os desenvolvedores de software que desejam criar aplicativos isolados que usarão os assemblies lado a lado disponibilizados pela Microsoft e por outros publicadores de assembly lado a lado.
-   Desenvolvedores de aplicativos interessados em criar seus próprios assemblies lado a lado para isolar seus aplicativos.
-   Administradores de rede que desejam mais informações sobre aplicativos isolados.

Como referência principal para compartilhamento de assembly lado a lado e aplicativos isolados, esta documentação fornece informações gerais básicas sobre a criação de manifestos e assemblies lado a lado, instalação de aplicativos isolados e assemblies lado a lado e uso da API de contexto de ativação.

## <a name="run-time-requirements"></a>Requisitos de tempo de execução

Windows o servidor 2003 e posterior ou Windows XP e posterior é necessário para usar assemblies e manifestos lado a lado para isolar aplicativos e usar a API de contexto de ativação.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                         | Descrição                                                                    |
|---------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Referência](side-by-side-assemblies-reference.md)<br/> | Documentação de aplicativos isolados e assemblies lado a lado.<br/> |



 

 

 




