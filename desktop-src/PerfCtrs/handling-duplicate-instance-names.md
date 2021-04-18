---
description: Embora os provedores sejam incentivados a usar nomes de instância exclusivos, nem todos os provedores.
ms.assetid: 3c8fcb8d-2ea4-4b24-b649-7bd375c1133d
title: Manipulando nomes de instância duplicada
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 220e5d7d0181a79c1d1415486cc946d484e11952
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105750778"
---
# <a name="handling-duplicate-instance-names"></a>Manipulando nomes de instância duplicada

Embora os provedores sejam altamente incentivados a usar nomes de instância exclusivos, nem todos os provedores fazem. A Convenção para exibir nomes de instâncias duplicadas é acrescentar um `#` caractere e um número de série ao nome da instância, com exceção da primeira ocorrência do nome. Por exemplo, se houver três instâncias de `svchost` em uma amostra, os três nomes serão exibidos como `svchost` , `svchost#1` e `svchost#2` .

Infelizmente, essa Convenção não resolve completamente o problema. Os números de série são atribuídos com base na ordem em que um nome de instância específico aparece em um exemplo, e essa ordem pode ser inconsistente de amostra para amostra. Por exemplo, um exemplo A pode ver `svchost` (pid 100), `svchost#1` (PID 200) e `svchost#2` (PID 300). Em seguida, se o svchost com PID 100 for desligado, o próximo exemplo verá `svchost` (pid 200) e `svchost#1` (PID 300). A lógica de correspondência básica tentaria corresponder as estatísticas de amostra A `svchost#1` (de pid 200) nas estatísticas de amostra b `svchost#1` (de PID 300), resultando em resultados inválidos para a amostra b. os erros ocorrem quando uma nova instância não exclusiva é exibida em uma amostra ou quando uma instância não exclusiva é interrompida em uma amostra (a menos que a instância adicionada/removida seja a última

## <a name="process-counterset"></a>Contador de processoset

Esse problema é especialmente problemático para o `Process` CounterSet porque ele usa apenas o nome do exe do processo como o nome da instância, mesmo que o nome do exe não seja exclusivo. O comportamento padrão do `Process` CounterSet no Windows não pode ser alterado devido a problemas de compatibilidade.

Você pode alterar o comportamento dos `Process` conjuntos e `Thread` configurados para usar nomes de instância exclusivos definindo `ProcessNameFormat` os `ThreadNameFormat` valores de registro ou na `HKLM\System\CurrentControlSet\Services\Perfproc\Performance` chave do registro.

> [!CAUTION]
> A habilitação de nomes de instância exclusivos para o `Process` CounterSet pode fazer com que alguns programas se comportem incorretamente, pois muitos programas esperam o padrão de nomenclatura não exclusivo. Por exemplo, um programa que está procurando uma instância com um nome de EXE conhecido específico não poderá mais encontrar essa instância depois de habilitar nomes de instância exclusivos.

O tipo de registro para esses valores é `REG_DWORD` . Definir o valor para `2` acrescentar o identificador do processo (PID) ao nome da instância do processo e o identificador de thread (TID) ao nome da instância do thread. Para desabilitar esse recurso, defina o valor como 1 ou exclua o valor.
