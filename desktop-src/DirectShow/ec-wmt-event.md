---
description: Enviado pelo filtro Leitor do WM ASF quando ele lê arquivos ASF protegidos pelo DRM (gerenciamento de direitos digitais).
ms.assetid: ac6ea7a1-238e-42ae-9f10-e1db60381357
title: EC_WMT_EVENT (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad2ae2659c26d170bef14a76c0528eb5159e92ef3598fb999215e1fbd848ea90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117819919"
---
# <a name="ec_wmt_event-dshowh"></a>EC_WMT_EVENT (Dshow.h)

Enviado pelo filtro [Leitor do WM ASF](wm-asf-reader-filter.md) quando ele lê arquivos ASF protegidos pelo DRM (gerenciamento de direitos digitais).

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*Lparam1*
</dt> <dd>

Um dos seguintes valores **de \_ STATUS do WMT:**



| Valor                         | Descrição                                                                                                       |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------|
| LICENÇA DE \_ AQUISIÇÃO DO WMT \_         | Enviado quando o componente DRM concluiu o processo de aquisição de licença, com êxito ou sem êxito. |
| WMT \_ INDIVIDUALIZE            | O processo de atualização de segurança foi concluído com êxito ou sem êxito.                                |
| O WMT \_ PRECISA \_ DE INDIVIDUALIZAÇÃO | O arquivo requer que um aplicativo receba uma atualização de segurança antes de executar a ação solicitada.          |
| WMT \_ SEM \_ DIREITOS               | O aplicativo não tem direitos para executar a ação solicitada em um arquivo protegido pelo DRM versão 1.                |
| WMT \_ NO \_ RIGHTS \_ EX           | O aplicativo não tem direitos para executar a ação solicitada em um arquivo protegido pelo DRM versão 7.                |



 

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Ponteiro para uma estrutura [**DE DADOS DE EVENTO \_ \_ WMT \_ AM**](/previous-versions/windows/desktop/api/evcode/ns-evcode-am_wmt_event_data) que contém informações sobre o evento ou **NULL.** O **membro pData** dessa estrutura aponta para dados adicionais, cujo tipo depende do valor **de lParam1,** conforme mostrado na tabela a seguir.



| Lparam1                       | AM \_ WMT \_ EVENT \_ DATA.pData                                                                                                                       |
|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| LICENÇA DE \_ AQUISIÇÃO DO WMT \_         | Ponteiro para uma [**estrutura WM GET LICENSE \_ \_ \_ DATA.**](/windows/desktop/wmformat/wm-get-license-data) Essa estrutura está documentada no SDK Windows Formato de Mídia. |
| WMT \_ INDIVIDUALIZE            | Ponteiro para uma [**estrutura WM \_ INDIVIDUALIZE \_ STATUS.**](/windows/desktop/wmformat/wm-individualize-status)                                                        |
| O WMT \_ PRECISA \_ DE INDIVIDUALIZAÇÃO | **NULL**.                                                                                                                                        |
| WMT \_ SEM \_ DIREITOS               | Ponteiro para uma cadeia de caracteres largos que contém uma URL de desafio.                                                                                   |
| WMT \_ NO \_ RIGHTS \_ EX           | Ponteiro para uma [**estrutura WM GET LICENSE \_ \_ \_ DATA.**](/windows/desktop/wmformat/wm-get-license-data)                                                               |



 

O valor de *lParam2* pode ser **NULL.** Verifique o valor antes de desreferenciar o ponteiro.

</dd> </dl>

## <a name="remarks"></a>Comentários

Consulte a Windows documentação do SDK de Formato de Mídia para obter mais informações sobre como habilenciar a reprodução de arquivos protegidos por DRM.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Códigos de notificação de eventos](event-notification-codes.md)
</dt> <dt>

[Notificação de eventos DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

