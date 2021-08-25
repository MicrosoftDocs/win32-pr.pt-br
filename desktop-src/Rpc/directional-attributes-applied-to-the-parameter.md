---
title: Atributos direcionais aplicados ao parâmetro
description: Os atributos direcionais \ in \ e \ out \ determinam como o cliente e o servidor alocam e liberam memória. A tabela a seguir resume o efeito de atributos direcionais na alocação de memória.
ms.assetid: 21ab54c4-a707-4ee3-bea8-8ba216e25c16
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e18e34a7ea553fd5c1fd9157877a0296e403443fc490bb328f48ac4b7b2c8b3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073386"
---
# <a name="directional-attributes-applied-to-the-parameter"></a>Atributos direcionais aplicados ao parâmetro

Os atributos direcionais \[ [dentro](/windows/desktop/Midl/in) \] e \[ [fora](/windows/desktop/Midl/out-idl) \] determinam como o cliente e o servidor alocam e liberam memória. A tabela a seguir resume o efeito de atributos direcionais na alocação de memória.



| Atributo direcional    | Memória no cliente                                                                                            | Memória no servidor                                                                                                                                        |
|--------------------------|-------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| \[[em](/windows/desktop/Midl/in)\]       | O aplicativo cliente deve alocar antes da chamada.                                                           | O stub do servidor é alocado.                                                                                                                                  |
| \[[out](/windows/desktop/Midl/out-idl)\] | O stub do cliente se aloca no retorno.                                                                            | O stub do servidor aloca somente o ponteiro de nível superior; o aplicativo de servidor deve alocar todos os ponteiros inseridos. O servidor também aloca novos dados conforme necessário. |
| \[**entrada**, **saída**\]      | O aplicativo cliente deve alocar dados iniciais transmitidos ao servidor; o stub do cliente aloca dados adicionais. | O stub do servidor aloca dados iniciais transmitidos do cliente; o aplicativo de servidor aloca novos dados conforme necessário.                                        |



 

Em todos esses casos, o stub do cliente não libera memória. O aplicativo cliente deve liberar a memória antes de ser encerrado. O stub de servidor libera memória quando a chamada de procedimento remoto retorna (sujeito ao \[ atributo [ALLOCATE](/windows/desktop/Midl/allocate) \] ACF).

 

 