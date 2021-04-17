---
description: Os tipos de dados com suporte pelo VDS definem valores de retorno de função, parâmetros de função e membros de estrutura. Os tipos de dados definem o tamanho e o significado desses elementos.
ms.assetid: f17e8c7e-e3cb-49ca-9060-2299dda55770
title: Tipos de dados VDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a868606110d9cf1c3cad5c3036789d041a5d86c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105797520"
---
# <a name="vds-data-types"></a>Tipos de dados VDS

\[A partir do Windows 8 e do Windows Server 2012, a interface com do [serviço de disco virtual](virtual-disk-service-portal.md) é substituída pela [API de gerenciamento de armazenamento do Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Os tipos de dados com suporte pelo VDS definem valores de retorno de função, parâmetros de função e membros de estrutura. Os tipos de dados definem o tamanho e o significado desses elementos.



| Tipo de dados                                                                                      | Descrição                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="VDS_OBJECT_ID"></span><span id="vds_object_id"></span>**\_ID do objeto VDS \_**<br/> | ID do objeto VDS. Não há garantia de que esses valores sejam exclusivos entre as reinicializações. <br/> Esse tipo é declarado em VDS. h (VdsHwPrv. h para provedores de hardware) como um GUID. <br/> |
| <span id="VDS_PATH_ID"></span><span id="vds_path_id"></span>**\_ID do caminho VDS \_**<br/>       | ID do caminho do VDS para e/s de vários caminhos (MPIO). <br/> Esse tipo é declarado em VDS. h (VdsHwPrv. h para provedores de hardware) como um UINT64.<br/>                                      |



 

 

