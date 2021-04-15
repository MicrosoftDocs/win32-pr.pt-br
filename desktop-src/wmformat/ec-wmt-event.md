---
title: EC_WMT_EVENT (SDK do Windows Media Format 11)
description: '\_evento de WMT do EC \_'
ms.assetid: 51d51659-8e7d-49b7-83f2-a80e99d39d78
keywords:
- SDK do Windows Media Format, EC_WMT_EVENT
- DirectShow, EC_WMT_EVENT
- EC_WMT_EVENT
- DRM (gerenciamento de direitos digitais), EC_WMT_EVENT
- DRM (gerenciamento de direitos digitais), EC_WMT_EVENT
- ASF (Advanced Systems Format), EC_WMT_EVENT
- ASF (formato de sistemas avançados), EC_WMT_EVENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebe74baaba676a97e609b4c03cd4db9010bd8f6a
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104454526"
---
# <a name="ec_wmt_event-windows-media-format-11-sdk"></a>EC_WMT_EVENT (SDK do Windows Media Format 11)

Enviado pelo Windows Media Format SDK quando um aplicativo usa o filtro de leitor de ASF para reproduzir arquivos ASF protegidos pelo DRM (gerenciamento de direitos digitais).

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

Ponteiro para uma estrutura de **\_ \_ \_ dados de evento WMT** que contém informações sobre o evento no ponteiro do membro **pData** , bem como um código de status **HRESULT** enviado pelo Windows Media Format SDK. O valor de *lParam2* depende do valor de *lParam1*, conforme descrito na tabela a seguir. (As estruturas "WM \_ " são definidas no Windows Media Format SDK.)



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

[**Referência do QASF do DirectShow**](directshow-qasf-reference.md)
</dt> <dt>

[**Habilitando o suporte a DRM**](enabling-drm-support.md)
</dt> </dl>

 

 




