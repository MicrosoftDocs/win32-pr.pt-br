---
title: Método IMsRdpClientNonScriptable NotifyRedirectDeviceChange
description: Notifica o módulo de redirecionamento de dispositivo do Área de Trabalho Remota controle ActiveX que ocorreu uma alteração de dispositivo no sistema. Esse método passa \_ notificações do WM DEVICECHANGE para o controle.
ms.assetid: 36323831-06e0-4e47-8a6c-06367119298f
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método NotifyRedirectDeviceChange
- Método NotifyRedirectDeviceChange Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable, método NotifyRedirectDeviceChange
- Método NotifyRedirectDeviceChange Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable2
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable2, método NotifyRedirectDeviceChange
- Método NotifyRedirectDeviceChange Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable3, método NotifyRedirectDeviceChange
- Método NotifyRedirectDeviceChange Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable4, método NotifyRedirectDeviceChange
- Método NotifyRedirectDeviceChange Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable5, método NotifyRedirectDeviceChange
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable.NotifyRedirectDeviceChange
- IMsRdpClientNonScriptable2.NotifyRedirectDeviceChange
- IMsRdpClientNonScriptable3.NotifyRedirectDeviceChange
- IMsRdpClientNonScriptable4.NotifyRedirectDeviceChange
- IMsRdpClientNonScriptable5.NotifyRedirectDeviceChange
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7357fcb5e31eeeb0de5791425b8d9fada4365ab8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919112"
---
# <a name="imsrdpclientnonscriptablenotifyredirectdevicechange-method"></a>Método IMsRdpClientNonScriptable:: NotifyRedirectDeviceChange

Notifica o módulo de redirecionamento de dispositivo do Área de Trabalho Remota controle ActiveX que ocorreu uma alteração de dispositivo no sistema. Esse método passa notificações do [**WM \_ DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) para o controle.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT NotifyRedirectDeviceChange(
  [in] WPARAM wParam,
  [in] LPARAM lParam
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* \[ no\]
</dt> <dd>

Especifica o evento do dispositivo. Esse parâmetro pode usar um dos valores a seguir.

<dt>

<span id="DBT_CONFIGCHANGECANCELED"></span><span id="dbt_configchangecanceled"></span>

<span id="DBT_CONFIGCHANGECANCELED"></span><span id="dbt_configchangecanceled"></span>**DBT \_ CONFIGCHANGECANCELED**


</dt> <dd>

Uma solicitação para alterar a configuração atual (Dock ou Dock) foi cancelada.

</dd> <dt>

<span id="DBT_CONFIGCHANGED"></span><span id="dbt_configchanged"></span>

<span id="DBT_CONFIGCHANGED"></span><span id="dbt_configchanged"></span>**DBT \_ ConfigChanged**


</dt> <dd>

A configuração atual foi alterada devido a um encaixe ou desencaixe.

</dd> <dt>

<span id="DBT_CUSTOMEVENT"></span><span id="dbt_customevent"></span>

<span id="DBT_CUSTOMEVENT"></span><span id="dbt_customevent"></span>**DBT \_ CUSTOMEVENT**


</dt> <dd>

Ocorreu um evento personalizado.

</dd> <dt>

<span id="DBT_DEVICEARRIVAL"></span><span id="dbt_devicearrival"></span>

<span id="DBT_DEVICEARRIVAL"></span><span id="dbt_devicearrival"></span>**DBT \_ DEVICEARRIVAL**


</dt> <dd>

Um dispositivo foi inserido e agora está disponível.

</dd> <dt>

<span id="DBT_DEVICEQUERYREMOVE"></span><span id="dbt_devicequeryremove"></span>

<span id="DBT_DEVICEQUERYREMOVE"></span><span id="dbt_devicequeryremove"></span>**DBT \_ DEVICEQUERYREMOVE**


</dt> <dd>

A permissão é solicitada para remover um dispositivo. Qualquer aplicativo pode negar essa solicitação e cancelar a remoção.

</dd> <dt>

<span id="DBT_DEVICEQUERYREMOVEFAILED"></span><span id="dbt_devicequeryremovefailed"></span>

<span id="DBT_DEVICEQUERYREMOVEFAILED"></span><span id="dbt_devicequeryremovefailed"></span>**DBT \_ DEVICEQUERYREMOVEFAILED**


</dt> <dd>

Uma solicitação para remover um dispositivo foi cancelada.

</dd> <dt>

<span id="DBT_DEVICEREMOVECOMPLETE"></span><span id="dbt_deviceremovecomplete"></span>

<span id="DBT_DEVICEREMOVECOMPLETE"></span><span id="dbt_deviceremovecomplete"></span>**DBT \_ DEVICEREMOVECOMPLETE**


</dt> <dd>

Um dispositivo foi removido.

</dd> <dt>

<span id="DBT_DEVICEREMOVEPENDING"></span><span id="dbt_deviceremovepending"></span>

<span id="DBT_DEVICEREMOVEPENDING"></span><span id="dbt_deviceremovepending"></span>**DBT \_ DEVICEREMOVEPENDING**


</dt> <dd>

Um dispositivo está prestes a ser removido. A remoção não pode ser negada.

</dd> <dt>

<span id="DBT_DEVICETYPESPECIFIC"></span><span id="dbt_devicetypespecific"></span>

<span id="DBT_DEVICETYPESPECIFIC"></span><span id="dbt_devicetypespecific"></span>**DBT \_ DEVICETYPESPECIFIC**


</dt> <dd>

Ocorreu um evento específico do dispositivo.

</dd> <dt>

<span id="DBT_DEVNODES_CHANGED"></span><span id="dbt_devnodes_changed"></span>

<span id="DBT_DEVNODES_CHANGED"></span><span id="dbt_devnodes_changed"></span>**DBT \_ DEVNODES \_ alterado**


</dt> <dd>

Um dispositivo foi adicionado ou removido do sistema.

</dd> <dt>

<span id="DBT_QUERYCHANGECONFIG"></span><span id="dbt_querychangeconfig"></span>

<span id="DBT_QUERYCHANGECONFIG"></span><span id="dbt_querychangeconfig"></span>**DBT \_ QUERYCHANGECONFIG**


</dt> <dd>

A permissão é solicitada para alterar a configuração atual (Dock ou desencaixar).

</dd> <dt>

<span id="DBT_USERDEFINED"></span><span id="dbt_userdefined"></span>

<span id="DBT_USERDEFINED"></span><span id="dbt_userdefined"></span>**DBT \_ USERdefined**


</dt> <dd>

O significado dessa mensagem é definido pelo usuário.

</dd> </dl> </dd> <dt>

*lParam* \[ no\]
</dt> <dd>

Ponteiro para uma estrutura que contém dados específicos do evento. Seu formato depende do valor do parâmetro *wParam* . Para obter mais informações, consulte a documentação de cada evento. Para obter mais informações, consulte [tipos de eventos de dispositivo](/windows/desktop/DevIO/device-event-types).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornar **S \_ OK** se for bem-sucedido.

## <a name="remarks"></a>Comentários

Um aplicativo de contêiner que permite a adição dinâmica ou remoção de dispositivos deve processar a mensagem do [**WM \_ DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) em sua janela de nível superior e encaminhar a mensagem para o controle usando o método **NotifyRedirectDeviceChange** . Um exemplo de uma alteração dinâmica do dispositivo é quando uma unidade de disco redirecionada é adicionada ou removida enquanto o sistema está em execução.

Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                     |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                               |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>       |
| IID<br/>                      | IID \_ IMsRdpClientNonScriptable é definido como 2f079c4c-87b2-4AFD-97ab-20cdb43038ae<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md)
</dt> <dt>

[**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md)
</dt> <dt>

[**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
</dt> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> <dt>

[**IMsRdpClientNonScriptable**](imsrdpclientnonscriptable-interface.md)
</dt> </dl>

 

