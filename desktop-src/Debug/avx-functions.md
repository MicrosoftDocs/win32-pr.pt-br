---
description: Funções do Intel AVX.
ms.assetid: 237f356a-9ee8-4c52-b08c-a6695c52713a
title: Funções AVX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b0b56c83b6beb674bc284b139bb656441956705
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104163900"
---
# <a name="avx-functions"></a>Funções AVX

A seguir estão as funções do Intel AVX.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                   | Descrição                                                                                                                    |
|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**CopyContext**](/windows/desktop/api/WinBase/nf-winbase-copycontext)<br/>                           | Copia uma estrutura de contexto de origem (incluindo qualquer XState) em uma estrutura de contexto de destino inicializada.<br/>         |
| [**GetEnabledXStateFeatures**](/windows/desktop/api/WinBase/nf-winbase-getenabledxstatefeatures)<br/> | Obtém uma máscara de recursos de XState habilitados em processadores x86 ou x64.<br/>                                                    |
| [**GetXStateFeaturesMask**](/windows/desktop/api/WinBase/nf-winbase-getxstatefeaturesmask)<br/>       | Retorna a máscara dos recursos do XState definidos em uma estrutura de [**contexto**](/windows/desktop/api/WinNT/ns-winnt-wow64_context) .<br/>                        |
| [**InitializeContext**](/windows/desktop/api/WinBase/nf-winbase-initializecontext)<br/>               | Inicializa uma estrutura de [**contexto**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) dentro de um buffer com o tamanho e o alinhamento necessários.<br/>       |
| [**LocateXStateFeature**](/windows/desktop/api/WinBase/nf-winbase-locatexstatefeature)<br/>           | Recupera um ponteiro para o estado do processador para um recurso XState dentro de uma estrutura de [**contexto**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) .<br/> |
| [**SetXStateFeaturesMask**](/windows/desktop/api/WinBase/nf-winbase-setxstatefeaturesmask)<br/>       | Define a máscara dos recursos do XState definidos em uma estrutura de [**contexto**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) .<br/>                             |



 

 

 




