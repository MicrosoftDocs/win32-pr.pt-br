---
description: Processo de alocação de recursos do dispensador de recursos
ms.assetid: 695d08f4-ba5c-4a5f-a2ad-481a8ede49ab
title: Processo de alocação de recursos do dispensador de recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a12cb22abd6d4d825f1ca048495b032a77fe216
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164017"
---
# <a name="resource-dispenser-resource-allocation-process"></a>Processo de alocação de recursos do dispensador de recursos

Cada vez que um dispensador de recursos aloca um recurso do seu detentor, ocorre o seguinte:

1.  O dispensador de recurso declara um identificador de tipo de recurso (**RESTYPID**), que descreve o tipo de recurso necessário.

2.  O dispensador de recurso chama o método [**IHolder:: AllocResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) do titular, passando esse **RESTYPID**.

3.  O detentor gera uma lista de candidatos dos recursos disponíveis. Os candidatos são recursos que não estão inscritos em uma transação ou já inscritos na transação do objeto de chamada.

4.  Esses candidatos são passados individualmente para o método [**IDispenserDriver:: RateResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-rateresource) , onde são classificados (em uma escala de 0 a 100) por quão bem o recurso candidato corresponde ao **RESTYPID** desejado.

5.  O detentor escolhe o recurso que o dispensador de recurso classifica como mais alto.

6.  O dispensador de recursos pode encerrar o loop de classificação no início, atribuindo ao candidato uma classificação de recursos de 100 (um ajuste perfeito). Uma classificação de 100 normalmente seria reservada para os recursos candidatos que já estão inscritos corretamente, a menos que o dispensador de recursos conclua que a inscrição é uma operação barata. Se todos os recursos candidatos (se houver) forem classificados como 0 (inutilizável), um novo recurso será criado chamando [**IDispenserDriver:: CreateResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-createresource).

7.  Se o recurso escolhido anteriormente ainda não estiver inscrito na transação do objeto de chamada, o método [**IDispenserDriver:: EnlistResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-enlistresource) do dispensador de recursos será chamado.

8.  A chamada do método [**AllocResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) retorna ao dispensador de recurso com o recurso inscrito.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conceitos do dispensador de recursos COM+](com--resource-dispenser-concepts.md)
</dt> <dt>

[Inlistando um recurso em uma transação](enlisting-a-resource-in-a-transaction.md)
</dt> <dt>

[Controlando recursos não alocados](tracking-non-allocated-resources.md)
</dt> </dl>

 

 



