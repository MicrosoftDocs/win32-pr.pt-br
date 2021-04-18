---
description: Lista os tipos de dados usados pelas DLLs de anexo de configuração de segurança e suas funções de suporte.
ms.assetid: 1d3bdf0d-320c-4b25-9e9b-fda134876979
title: Tipos de dados de gerenciamento de segurança
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae7efedb32ab545b903c61819042e32b7d83dbf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105753387"
---
# <a name="security-management-data-types"></a>Tipos de dados de gerenciamento de segurança

Os tipos de dados de gerenciamento de segurança incluem o seguinte:

-   [Tipos de dados de anexo](#attachment-data-types)
-   [Tipos de dados de política LSA](#lsa-policy-data-types)

## <a name="attachment-data-types"></a>Tipos de dados de anexo

Os tipos de dados a seguir são usados pelas DLLs de anexo de configuração de segurança e suas funções de suporte.



| Tipo de dados                                                    | Descrição                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_contexto de enumeração do SCE \_**](sce-enumeration-context.md) | Usado pela função [**de \_ \_ informações de consulta PFSCE**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) para navegar pelo banco de dados de segurança.                                                                                                                                              |
| [**identificador do SCE \_**](sce-handle.md)                            | Usado por [**\_ \_ informações de consulta PFSCE**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) e [**PFSCE \_ definir \_**](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info) informações para passar informações entre o anexo e o banco de dados de segurança.                                                                                 |
| [**SCESTATUS**](scestatus.md)                               | O tipo de dados é usado pela API do conjunto de ferramentas de configuração de segurança para retornar informações sobre os resultados de uma chamada de função.                                                                                                                                    |
| [**identificador de SCESVC \_**](scesvc-handle.md)                      | Usado por métodos das interfaces [**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata) e [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo) para passar informações entre o snap-in de configuração de segurança e a extensão do snap-in. |
| [**\_tipo de informação SCESVC \_**](/windows/desktop/api/Scesvc/ne-scesvc-scesvc_info_type)               | A enumeração é usada pelas informações de [**consulta do PFSCE \_ \_**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) e pelo [**PFSCE \_ set \_ info**](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info) para indicar o tipo de informações solicitadas ou passadas para o banco de dados de segurança.                                                 |



 

## <a name="lsa-policy-data-types"></a>Tipos de dados de política LSA

Os tipos de dados a seguir são usados pelas funções de gerenciamento de política do LSA.



| Tipo de dados                                                  | Descrição                                                               |
|------------------------------------------------------------|---------------------------------------------------------------------------|
| [**\_identificador de enumeração LSA \_**](lsa-enumeration-handle.md) | Usado para rastrear enumerações nas quais várias chamadas de função são necessárias. |
| [**identificador de LSA \_**](lsa-handle.md)                          | Identificador para um objeto de [**política**](policy-object.md) .                       |



 

 

 
