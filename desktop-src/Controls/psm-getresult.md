---
title: Mensagem de PSM_GETRESULT (Prsht. h)
description: Usado por folhas de propriedades sem janela restrita para recuperar as informações retornadas às folhas de propriedades modais por folha. Você pode enviar essa mensagem explicitamente ou usar a \_ macro GetResult PropSheet.
ms.assetid: e0f609ea-5d7e-4c17-ade1-3c1051c5a5bf
keywords:
- Controles de PSM_GETRESULT de mensagens do Windows
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
ms.openlocfilehash: d41609f625cbd3938fa78e9a2f91ab70168ecc29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499625"
---
# <a name="psm_getresult-message"></a>Mensagem de PSM \_ GETresult

Usado por folhas de propriedades sem janela restrita para recuperar as informações retornadas às folhas de propriedades modais por [**folha**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta). Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ GetResult PropSheet**](/windows/desktop/api/Prsht/nf-prsht-propsheet_getresult) .

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

## <a name="return-value"></a>Retornar valor

Retorna um valor positivo se for bem-sucedido ou-1 caso contrário. Os valores de retorno a seguir têm um significado especial.



| Código de retorno                                                                                         | Descrição                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ID \_ PSREBOOTSYSTEM**</dt> </dl>   | Uma página enviou uma mensagem de [**PSM \_ REBOOTSYSTEM**](psm-rebootsystem.md) para a folha de propriedades. O computador deve ser reiniciado para que as alterações do usuário entrem em vigor.<br/> |
| <dl> <dt>**ID \_ PSRESTARTWINDOWS**</dt> </dl> | Uma página enviou uma mensagem de [**PSM \_ RESTARTWINDOWS**](psm-restartwindows.md) para a folha de propriedades. O Windows deve ser reiniciado para que as alterações do usuário entrem em vigor.<br/>  |



 

## <a name="remarks"></a>Comentários

Para recuperar informações de erro estendidas, chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

O valor de retorno para essa mensagem é idêntico ao que [**folha**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) retorna para uma folha de propriedades modal.

[Versão 5,80.](common-control-versions.md) O valor de retorno [**folha**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) transporta informações diferentes para folhas de propriedades modais e sem janela restrita. Em alguns casos, as folhas de propriedades sem janela restrita podem precisar das informações recebidas de **folha** se tivessem sido modais. Em particular, talvez seja necessário saber se a ID \_ PSREBOOTSYSTEM ou a ID \_ PSRESTARTWINDOWS teria sido retornada.

Para uma folha de propriedades sem janela restrita, o loop de mensagem deve usar o [**PSM \_ ISDIALOGMESSAGE**](psm-isdialogmessage.md) para passar as mensagens para a caixa de diálogo da folha de propriedades e o [**PSM \_ GETCURRENTPAGEHWND**](psm-getcurrentpagehwnd.md) para determinar quando destruir a caixa de diálogo. Quando o usuário clica no botão **OK** ou **Cancelar** , o **PSM \_ GETCURRENTPAGEHWND** retorna **nulo**. Em seguida, você pode recuperar o valor que uma folha de propriedades modal teria recebido de [**folha**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) enviando uma mensagem de **PSM \_ GetResult** .

> [!Note]  
> Não há suporte para esta mensagem ao usar o estilo de assistente Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

