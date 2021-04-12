---
title: Serviços base do TPM
description: O software TPM fornece serviços como uma API exposta por meio de chamada de procedimento remoto. Use o TPM para criar um módulo TPM.
ms.assetid: ae6e7fe9-585d-467a-8456-e008b8ea89a0
keywords:
- TBS dos serviços de base do TPM
- TBS de serviços base do TPM, home page
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d2cbdfc1f85d6917f2e9a7a5b8e7a0fc25ebdc8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366379"
---
# <a name="tpm-base-services"></a>Serviços base do TPM

## <a name="purpose"></a>Finalidade

O recurso TBS (serviços base) do Trusted Platform Module (TPM) centraliza o acesso do TPM entre aplicativos.

O recurso TBS é executado como um serviço de sistema no Windows Server 2008, no Windows Vista ou em sistemas operacionais mais recentes. Ele fornece serviços como uma API exposta por meio de chamadas de procedimento remoto (RPC). O recurso TBS usa prioridades especificadas chamando aplicativos para agendar de acordo com o acesso do TPM.

> [!Note]
>
> O TPM pode ser usado para operações de armazenamento de chaves. No entanto, os desenvolvedores são incentivados a usar as [principais APIs de armazenamento](/windows/desktop/SecCNG/key-storage-and-retrieval) para esses cenários. As APIs de armazenamento de chaves fornecem a funcionalidade para criar, assinar ou criptografar e manter chaves criptográficas, e elas são de nível superior e mais fáceis de usar do que os TBS para esses cenários de destino.

 

## <a name="developer-audience"></a>Público de desenvolvedores

O TBS destina-se ao uso por desenvolvedores de aplicativos baseados nos sistemas operacionais Windows. Os desenvolvedores devem estar familiarizados com as linguagens de programação C e C++ e o ambiente de programação do Microsoft Windows.

## <a name="run-time-requirements"></a>Requisitos de tempo de execução

O recurso TBS requer pelo menos o sistema operacional Windows Server 2008 ou Windows Vista. Para obter informações sobre os requisitos de tempo de execução para um determinado elemento de programação, consulte a seção requisitos da página de referência para esse elemento.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                         | Descrição                                                                     |
|-----------------------------------------------|---------------------------------------------------------------------------------|
| [Sobre TBS](about-tbs.md)<br/>         | Conceitos principais e uma exibição de alto nível do recurso TBS.<br/>               |
| [Usando TBS](using-tbs.md)<br/>         | Processos e procedimentos TBS para usar a API TBS.<br/>                  |
| [Referência de TBS](tbs-reference.md)<br/> | Documentação sobre as funções, estruturas e códigos de retorno do TBS.<br/> |



 

 

