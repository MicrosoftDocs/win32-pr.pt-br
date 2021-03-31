---
description: Um programa de configuração usa a função CreateService para instalar um novo serviço no banco de dados SCM.
ms.assetid: 554b9983-4e49-4b11-b420-a4754123d854
title: Instalação, remoção e enumeração de serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1069bba094205efd3257063a89c74326b2806455
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647039"
---
# <a name="service-installation-removal-and-enumeration"></a>Instalação, remoção e enumeração de serviço

Um programa de configuração usa a função [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) para instalar um novo serviço no banco de dados SCM. Essa função especifica o nome do serviço e fornece informações de configuração que são armazenadas no banco de dados. Para obter uma descrição das informações armazenadas no banco de dados para cada serviço, consulte [banco de dados dos serviços instalados](database-of-installed-services.md). Para obter um exemplo de código, consulte [instalando um serviço](installing-a-service.md).

Um programa de configuração usa a função [**DeleteService**](/windows/desktop/api/Winsvc/nf-winsvc-deleteservice) para remover um serviço instalado do banco de dados. Para obter mais informações, consulte [excluindo um serviço](deleting-a-service.md).

Para obter o nome do serviço, chame a função [**GetServiceKeyName**](/windows/desktop/api/Winsvc/nf-winsvc-getservicekeynamea) . O nome de exibição do serviço, usado no miniaplicativo do painel de controle de serviços, pode ser obtido chamando a função [**GetServiceDisplayName**](/windows/desktop/api/Winsvc/nf-winsvc-getservicedisplaynamea) .

Um programa de configuração de serviço pode usar a função [**EnumServicesStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa) para enumerar todos os serviços e seus status. Ele também pode usar a função [**EnumDependentServices**](/windows/desktop/api/Winsvc/nf-winsvc-enumdependentservicesa) para enumerar quais serviços dependem de um objeto de serviço especificado.

 

 



