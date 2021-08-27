---
title: Estruturas de plug-in
description: estruturas para desenvolvimento de aplicativo cliente pela API de Windows Biometric Framework.
ms.assetid: 64fb908c-72c2-4639-a2f6-77ede080512c
keywords:
- Windows api do Framework de biométrica Windows Biometric Framework apis, estruturas de plug-in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e150dd043a8c95e91d0f9095e23584544f43a503a709ae54c9180e06aa40bdaf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101236"
---
# <a name="plug-in-structures"></a>Estruturas de plug-in

as estruturas a seguir têm suporte para o desenvolvimento de aplicativos cliente pela API Windows Biometric Framework.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                                | Descrição                                                                                                                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**\_política de conta do WINBIO \_**](winbio-account-policy.md)<br/>                                  | Contém uma política de antifalsificação padrão ou específica da conta.<br/>                                                         |
| [**\_versão da \_ interface do adaptador WINBIO \_**](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_adapter_interface_version)<br/>           | Contém um número de versão principal e secundária usado nas tabelas do mecanismo, do sensor e da interface do adaptador de armazenamento.<br/>                |
| [**\_interface do mecanismo do WINBIO \_**](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_engine_interface)<br/>                              | Contém ponteiros para suas funções de adaptador de mecanismo personalizadas.<br/>                                                                 |
| [**\_parâmetros de \_ registro ESTENDIdo WINBIO \_**](winbio-extended-enrollment-parameters.md)<br/> | Contém informações adicionais que um adaptador de mecanismo precisa para criar um modelo de registro. <br/>                            |
| [**PIPELINE de WINBIO \_**](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_pipeline)<br/>                                               | Contém informações de contexto compartilhado usadas pelos componentes do sensor, do mecanismo e do adaptador de armazenamento em uma única unidade biométrica.<br/> |
| [**\_interface do sensor WINBIO \_**](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_sensor_interface)<br/>                              | Contém ponteiros para as funções do adaptador do sensor personalizado.<br/>                                                                 |
| [**\_interface de armazenamento WINBIO \_**](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_storage_interface)<br/>                            | Contém ponteiros para suas funções de adaptador de armazenamento personalizadas.<br/>                                                                |
| [**\_registro de armazenamento WINBIO \_**](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_storage_record)<br/>                                  | Contém um modelo biométrico e dados associados em um formato padrão.<br/>                                                    |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de plug-in](plug-in-reference.md)
</dt> <dt>

[Funções de plug-in](plug-in-functions.md)
</dt> <dt>

[**WbioQueryEngineInterface**](/windows/desktop/api/Winbio_adapter/nf-winbio_adapter-wbioqueryengineinterface)
</dt> <dt>

[**WbioQuerySensorInterface**](/windows/desktop/api/Winbio_adapter/nf-winbio_adapter-wbioquerysensorinterface)
</dt> <dt>

[**WbioQueryStorageInterface**](/windows/desktop/api/Winbio_adapter/nf-winbio_adapter-wbioquerystorageinterface)
</dt> </dl>

 

 





