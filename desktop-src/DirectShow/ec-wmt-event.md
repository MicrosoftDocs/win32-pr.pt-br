---
description: Enviado pelo filtro de leitor ASF do WM quando ele lê arquivos ASF protegidos pelo DRM (gerenciamento de direitos digitais).
ms.assetid: ac6ea7a1-238e-42ae-9f10-e1db60381357
title: EC_WMT_EVENT (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8ce974cd83a404242fb51486f0889ac9b79e044
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752678"
---
# <a name="ec_wmt_event-dshowh"></a>EC_WMT_EVENT (DShow. h)

Enviado pelo filtro de [leitor ASF do WM](wm-asf-reader-filter.md) quando ele lê arquivos ASF protegidos pelo DRM (gerenciamento de direitos digitais).

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Um dos seguintes valores **de \_ status de WMT** :



| Valor                         | Descrição                                                                                                       |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------|
| \_licença de aquisição do WMT \_         | Enviado quando o componente DRM concluiu o processo de aquisição de licença, seja com êxito ou sem êxito. |
| \_individualizar WMT            | O processo de atualização de segurança foi concluído com êxito ou não.                                |
| WMT \_ precisa de \_ individualização | O arquivo requer que um aplicativo receba uma atualização de segurança antes de executar a ação solicitada.          |
| WMT \_ sem \_ direitos               | O aplicativo não tem direitos para executar a ação solicitada em um arquivo protegido pelo DRM versão 1.                |
| WMT \_ sem \_ direitos \_ ex           | O aplicativo não tem direitos para executar a ação solicitada em um arquivo protegido pelo DRM versão 7.                |



 

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Ponteiro para uma estrutura de [**\_ \_ \_ dados de evento WMT**](/previous-versions/windows/desktop/api/evcode/ns-evcode-am_wmt_event_data) que contém informações sobre o evento ou **NULL**. O membro **pData** dessa estrutura aponta para dados adicionais, cujo tipo depende do valor de **lParam1**, conforme mostrado na tabela a seguir.



| lParam1                       | \_WMT \_ dados de evento am \_ . pData                                                                                                                       |
|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| \_licença de aquisição do WMT \_         | Ponteiro para uma estrutura de [**\_ \_ \_ dados obter licença do WM**](/windows/desktop/wmformat/wm-get-license-data) . Essa estrutura está documentada no Windows Media Format SDK. |
| \_individualizar WMT            | Ponteiro para uma estrutura de [**\_ \_ status de individualização do WM**](/windows/desktop/wmformat/wm-individualize-status) .                                                        |
| WMT \_ precisa de \_ individualização | **NULL**.                                                                                                                                        |
| WMT \_ sem \_ direitos               | Ponteiro para uma cadeia de caracteres largos contendo uma URL de desafio.                                                                                   |
| WMT \_ sem \_ direitos \_ ex           | Ponteiro para uma estrutura de [**\_ \_ \_ dados obter licença do WM**](/windows/desktop/wmformat/wm-get-license-data) .                                                               |



 

O valor de *lParam2* pode ser **nulo**. Verifique o valor antes de cancelar a referência ao ponteiro.

</dd> </dl>

## <a name="remarks"></a>Comentários

Consulte a documentação do SDK do Windows Media Format para obter mais informações sobre como habilitar a reprodução de arquivos protegidos por DRM.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Códigos de notificação de eventos](event-notification-codes.md)
</dt> <dt>

[Notificação de eventos no DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

