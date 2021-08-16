---
title: Antimalware de início antecipado
description: Antimalware de início antecipado
ms.assetid: 4064CD44-FC50-48DE-8490-F592ED21CB7E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f1ca8e52f9d2465038e68b6b585bed70b974432566b3b67d080c97bb998103f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117852192"
---
# <a name="early-launch-antimalware"></a>Antimalware de início antecipado

## <a name="platforms"></a>Plataformas

 **clientes** -Windows 8  
**servidores** -Windows Server 2012  

## <a name="description"></a>Descrição

Como o software antimalware (AM) se tornou melhor e melhor na detecção de malware de tempo de execução, os invasores também estão se tornando melhores na criação de rootkits que podem se esconder da detecção. Detectar malwares que iniciam no início do ciclo de inicialização é um desafio que a maioria dos fornecedores nos atendem de maneira programada. Normalmente, eles criam hackers do sistema que não têm suporte no sistema operacional do host e podem realmente resultar na colocação do computador em um estado instável. até este ponto, Windows não forneceu uma boa maneira para que eu detecte e resolva essas ameaças de inicialização antecipada.

Windows 8 apresenta um novo recurso chamado inicialização segura, que protege os componentes e a configuração de inicialização do Windows e carrega um driver ELAM (antimalware de início antecipado). esse driver começa antes de outros drivers de inicialização e habilita a avaliação desses drivers e ajuda o kernel Windows a decidir se eles devem ser inicializados.

## <a name="manifestation"></a>Manifestação

Ao ser iniciado primeiro pelo kernel, o ELAM é garantido para ser iniciado antes de qualquer software de terceiros e, portanto, é capaz de detectar malware no processo de inicialização e impedir a inicialização.

## <a name="mitigation"></a>Atenuação

Os drivers de inicialização são inicializados com base na classificação retornada pelo driver ELAM de acordo com uma política de inicialização. Por padrão, a política Inicializa drivers bons e desconhecidos conhecidos, mas não inicializa drivers inválidos conhecidos. Um administrador do sistema pode especificar uma política personalizada por meio de Política de Grupo que pode impedir a inicialização de drivers desconhecidos ou a habilitação de drivers que são críticos para o processo de inicialização, mas foram adulterados, inicializados para inicialização.

## <a name="solution"></a>Solução

Um driver ELAM deve se registrar para retornos de chamada de kernel para obter informações sobre cada driver de inicialização inicial à medida que ele está sendo inicializado. O driver ELAM pode retornar uma classificação para cada driver. Essas funções são necessárias:

-   [IoRegisterBootDriverCallback](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-ioregisterbootdrivercallback)
-   [IoUnRegisterBootDriverCallback](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-iounregisterbootdrivercallback)

Um driver ELAM também pode se registrar para retornos de chamada do registro. Isso permite que o driver ELAM Inspecione os dados de configuração que são usados por cada driver de inicialização inicial. O driver ELAM pode, então, bloquear ou modificar os dados antes que eles sejam usados pelos drivers de inicialização inicial, se necessário. Essas funções são necessárias:

-   [CmRegisterCallbackEx](/windows-hardware/drivers/ddi/wdm/nf-wdm-cmregistercallbackex)
-   [CmUnRegisterCallback](/windows-hardware/drivers/ddi/wdm/nf-wdm-cmunregistercallback)

Para obter mais detalhes sobre os requisitos do driver ELAM e o uso da API, consulte [pré-malware de início antecipado](/windows-hardware/drivers/install/early-launch-antimalware).

## <a name="tests"></a>Testes

os drivers ELAM devem ser assinados especialmente pela Microsoft para garantir que eles sejam iniciados pelo kernel Windows no início do processo de inicialização. Para obter a assinatura, os drivers ELAM devem passar um conjunto de testes de certificação para verificar o desempenho e outros comportamentos. esses testes estão incluídos no Kit de certificação de Hardware Windows.

## <a name="resources"></a>Recursos

-   [AntiMalware de início antecipado](/windows-hardware/drivers/install/early-launch-antimalware)
-   [CmRegisterCallbackEx](/windows-hardware/drivers/ddi/wdm/nf-wdm-cmregistercallbackex)
-   [CmUnRegisterCallback](/windows-hardware/drivers/ddi/wdm/nf-wdm-cmunregistercallback)
-   [IoRegisterBootDriverCallback](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-ioregisterbootdrivercallback)
-   [IoUnRegisterBootDriverCallback](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-iounregisterbootdrivercallback)
-   [certificando o hardware com a Windows apresentação da conferência de Build do Kit de certificação de hardware](https://channel9.msdn.com/events/BUILD/BUILD2011/HW-659T)
-   [Baixar kits e ferramentas](https://msdn.microsoft.com/windows/hardware/br259105)

 

 
