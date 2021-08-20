---
title: PSM_GETRESULT mensagem (Prsht.h)
description: Usado por folhas de propriedades sem modo para recuperar as informações retornadas para folhas de propriedades modais por PropertySheet. Você pode enviar essa mensagem explicitamente ou usar a \_ macro GetResult do PropSheet.
ms.assetid: e0f609ea-5d7e-4c17-ade1-3c1051c5a5bf
keywords:
- PSM_GETRESULT controles de Windows mensagem
topic_type:
- apiref
api_name:
- PSM_GETRESULT
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4acc8fed8cdaa1f4282c3ed066ad44f68221330fa9e79b0719db8bba1bca37f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118169802"
---
# <a name="psm_getresult-message"></a>Mensagem GETRESULT do PSM \_

Usado por folhas de propriedades sem modo para recuperar as informações retornadas para folhas de propriedades modais por [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta). Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ GetResult do PropSheet.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_getresult)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará um valor positivo se for bem-sucedido ou -1 caso contrário. Os valores de retorno a seguir têm um significado especial.



| Código de retorno                                                                                         | Descrição                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ID \_ PSREBOOTSYSTEM**</dt> </dl>   | Uma página enviou uma [**mensagem \_ REBOOTSYSTEM do PSM**](psm-rebootsystem.md) para a folha de propriedades. O computador deve ser reiniciado para que as alterações do usuário entre em vigor.<br/> |
| <dl> <dt>**ID \_ PSRESTARTWINDOWS**</dt> </dl> | Uma página enviou uma [**mensagem \_ RESTARTWINDOWS do PSM**](psm-restartwindows.md) para a folha de propriedades. Windows deve ser reiniciado para que as alterações do usuário entre em vigor.<br/>  |



 

## <a name="remarks"></a>Comentários

Para recuperar informações de erro estendidas, [**chame GetLastError.**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)

O valor de retorno dessa mensagem é idêntico ao que [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) retorna para uma folha de propriedades modal.

[Versão 5.80.](common-control-versions.md) O valor de retorno [**propertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) carrega informações diferentes para folhas de propriedades modais e sem modo. Em alguns casos, as folhas de propriedades sem modo podem precisar das informações que teriam recebido do **PropertySheet** se elas tivessem sido modais. Em particular, talvez eles precisem saber se a ID \_ PSREBOOTSYSTEM ou ID \_ PSRESTARTWINDOWS teria sido retornada.

Para uma folha de propriedades sem modo, o loop de mensagem deve usar [**\_ ISDIALOGMESSAGE PSM**](psm-isdialogmessage.md) para passar mensagens para a caixa de diálogo da folha de propriedades e [**\_ GETCURRENTPAGEHWND do PSM**](psm-getcurrentpagehwnd.md) para determinar quando destruir a caixa de diálogo. Quando o usuário clica no **botão OK** ou **Cancelar,** **O PSM \_ GETCURRENTPAGEHWND** retorna **NULL.** Em seguida, você pode recuperar o valor que uma folha de propriedades modal teria recebido de [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) enviando uma **mensagem \_ GETRESULT PSM.**

> [!Note]  
> Não há suporte para essa mensagem ao usar o estilo do assistente do Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

