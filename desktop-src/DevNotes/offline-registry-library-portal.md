---
description: Biblioteca de registro offline
ms.assetid: 5861e0a9-6a3f-4bc8-ae8b-d51c9de28217
title: Biblioteca de registro offline
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae1aa5acdd7904516608413ff973e60e81c296c3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089244"
---
# <a name="offline-registry-library"></a>Biblioteca de registro offline

## <a name="purpose"></a>Finalidade

A biblioteca de registro offline (Offreg.dll) é usada para modificar um hive do registro fora do registro do sistema ativo. Essa biblioteca destina-se a cenários de atualização de registro, como manutenção de uma imagem do sistema operacional. A biblioteca dá suporte aos formatos do hive do registro a partir do Windows Vista.

## <a name="developer-audience"></a>Público de desenvolvedores

Essa tecnologia é para OEMs (fabricantes de equipamento original), fornecedores de software antivírus e antimalware e outros desenvolvedores de aplicativos que devem ser capazes de analisar arquivos do hive do registro sem carregá-los no registro ativo.

## <a name="run-time-requirements"></a>Requisitos de tempo de execução

A biblioteca de registro offline é fornecida como uma DLL (biblioteca de vínculo dinâmico) redistribuível binária. Essa biblioteca é executada nas seguintes versões do Windows:

<dl> Windows Server 2016  
Windows 10  
Windows 8.1  
Windows Server 2012 R2  
Windows 8  
Windows Server 2012  
Windows 7  
Windows Server 2008 R2  
Windows Server 2008  
Windows Vista  
</dl>

Os aplicativos devem ser vinculados a Offreg.dll usando vinculação dinâmica.

O Offreg.dll é fornecido no Windows Driver Kit (WDK) para Windows 10 e versões anteriores do sistema operacional Windows.

Para obter informações sobre como obter o WDK, consulte [como obter o WDK e o WLK](/windows-hardware/drivers/download-the-wdk) ou visite o site de [assinaturas do MSDN](https://msdn.microsoft.com/subscriptions/default.aspx) .

## <a name="in-this-section"></a>Nesta seção

-   [**Sobre a biblioteca de registro offline**](about-the-offline-registry-library.md)
-   [**Funções da biblioteca do registro offline**](offline-registry-library-functions.md)

 

 
