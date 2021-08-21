---
title: EC_WMT_EVENT (SDK do formato de mídia 11 Windows)
description: '\_evento de WMT do EC \_'
ms.assetid: 51d51659-8e7d-49b7-83f2-a80e99d39d78
keywords:
- Windows SDK do formato de mídia, EC_WMT_EVENT
- DirectShow, EC_WMT_EVENT
- EC_WMT_EVENT
- DRM (gerenciamento de direitos digitais), EC_WMT_EVENT
- DRM (gerenciamento de direitos digitais), EC_WMT_EVENT
- ASF (Advanced Systems Format), EC_WMT_EVENT
- ASF (formato de sistemas avançados), EC_WMT_EVENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbe0e53a759515914a352707550e281aca3aebe096f168352c36c1ff4200b2ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118029215"
---
# <a name="ec_wmt_event-windows-media-format-11-sdk"></a>EC_WMT_EVENT (SDK do formato de mídia 11 Windows)

enviado pelo SDK do formato de mídia Windows quando um aplicativo usa o filtro de leitor de asf para reproduzir arquivos ASF protegidos pelo DRM (gerenciamento de direitos digitais).

Parâmetros

*lParam1*

Pode ser um dos seguintes valores de \_ status de WMT.



| Mensagem de status do WMT \_           | Descrição                                                                                                                    |
|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| WMT \_ sem \_ direitos               | O arquivo é protegido com o DRM versão 1 e o aplicativo não tem direitos para executar a ação solicitada.                    |
| \_licença de aquisição do WMT \_         | O processo de aquisição de licença foi concluído. (Isso não significa, necessariamente, que uma licença foi adquirida com êxito.) |
| WMT \_ sem \_ direitos \_ ex           | O arquivo é protegido com o DRM versão 7 e o aplicativo não tem direitos para executar a ação solicitada.                    |
| WMT \_ precisa de \_ individualização | A licença permite que somente aplicativos individualizados executem a ação solicitada.                                           |
| \_individualizar WMT            | O processo de individualização agora está sendo executado ou foi concluído.                                                    |



 

*lParam2*

ponteiro para uma estrutura de **\_ \_ \_ dados de evento WMT** que contém informações sobre o evento no ponteiro do membro **pData** , bem como um código de status **HRESULT** enviado pelo SDK do formato de mídia Windows. O valor de *lParam2* depende do valor de *lParam1*, conforme descrito na tabela a seguir. (as estruturas "WM \_ " são definidas no SDK do formato de mídia Windows.)



| Se lParam1 for...              | AM \_ WMT \_ Event \_ Data. pData is...                            |
|-------------------------------|-------------------------------------------------------------|
| WMT \_ sem \_ direitos               | Um ponteiro para uma cadeia de caracteres **WCHAR** que contém uma URL de desafio. |
| \_licença de aquisição do WMT \_         | Um ponteiro para uma estrutura de **\_ \_ \_ dados obter licença do WM** .        |
| WMT \_ sem \_ direitos \_ ex           | Um ponteiro para uma estrutura de **\_ \_ \_ dados obter licença do WM** .        |
| WMT \_ precisa de \_ individualização | NULL.                                                       |
| \_individualizar WMT            | Um ponteiro para uma estrutura de **\_ \_ status de individualização do WM** .     |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Recursos de Rights Management digital**](digital-rights-management-features.md)
</dt> <dt>

[**DirectShow Referência de QASF**](directshow-qasf-reference.md)
</dt> <dt>

[**Habilitando o suporte a DRM**](enabling-drm-support.md)
</dt> </dl>

 

 




