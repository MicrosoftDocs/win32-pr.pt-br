---
title: Método IWMDRMDeviceApp SynchronizeLicenses (WMDRMDeviceApp. h)
description: O método SynchronizeLicenses atualiza licenças em um dispositivo quando elas estão próximas de expirar.
ms.assetid: 352378c1-7432-476c-98e9-d811165c020e
keywords:
- Método SynchronizeLicenses Windows Media Gerenciador de Dispositivos
- Método SynchronizeLicenses Windows Media Gerenciador de Dispositivos, interface IWMDRMDeviceApp
- Interface IWMDRMDeviceApp Windows Media Gerenciador de Dispositivos, método SynchronizeLicenses
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp.SynchronizeLicenses
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91ec48743bf52d990c64ce1aecf30897a7ee2f51664e88695a181f9d4f758140
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031736"
---
# <a name="iwmdrmdeviceappsynchronizelicenses-method"></a>Método IWMDRMDeviceApp:: SynchronizeLicenses

O método **SynchronizeLicenses** atualiza licenças em um dispositivo quando elas estão próximas de expirar.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SynchronizeLicenses(
  [in] IWMDMDevice    *pDevice,
  [in] IWMDMProgress3 *pProgressCallback,
  [in] DWORD          cMinCountThreshold,
  [in] DWORD          cMinHoursThreshold
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDevice* \[ no\]
</dt> <dd>

Ponteiro para um objeto [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) .

</dd> <dt>

*pProgressCallback* \[ no\]
</dt> <dd>

O retorno de chamada de progresso que receberá o progresso de todas as etapas que talvez precisem ser executadas. A etapa é identificada pelo parâmetro *EventID* do método [**IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3) chamado.

</dd> <dt>

*cMinCountThreshold* \[ no\]
</dt> <dd>

Contagem mínima opcional de execuções pendentes em uma licença de dispositivo.

</dd> <dt>

*cMinHoursThreshold* \[ no\]
</dt> <dd>

Mínimo opcional de horas restantes em uma licença de dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                                                         | Descrição                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                | O método foi bem-sucedido.<br/>                                                                                                                            |
| <dl> <dt>**DRM \_ E \_ INVALIDARG**</dt> </dl>                   | Um ou mais argumentos não são válidos.<br/>                                                                                                             |
| <dl> <dt>**DRM \_ E \_ INVALIDXMLTAG**</dt> </dl>                | O XML está formado incorretamente.<br/>                                                                                                                        |
| <dl> <dt>**DRM \_ E \_ NOTIMPL**</dt> </dl>                      | Essa funcionalidade não está implementada no momento. (SyncLicenses w/ *pDevice* = NULL)<br/>                                                               |
| <dl> <dt>**DRM \_ E \_ NOXMLCLOSETAG**</dt> </dl>                | O XML de licença foi formado incorretamente.<br/>                                                                                                           |
| <dl> <dt>**DRM \_ E \_ NOXMLOPENTAG**</dt> </dl>                 | O XML de licença foi formado incorretamente.<br/>                                                                                                           |
| <dl> <dt>**o DRM \_ E a \_ OUTOFMEMORY**</dt> </dl>                  | Sem memória.<br/>                                                                                                                                   |
| <dl> <dt>**DRM \_ E \_ XMLNOTFOUND**</dt> </dl>                  | Falha ao localizar uma marca XML necessária na licença.<br/>                                                                                                |
| <dl> <dt>**dispositivo \_ ns \_ E \_ não \_ WMDRM \_**</dt> </dl>    | o dispositivo especificado não é um dispositivo compatível com DRM com mídia Windows.<br/>                                                                               |
| <dl> <dt>**o NS \_ E \_ DRM precisa de \_ \_ individualização**</dt> </dl> | O DRM requer uma caixa preta individual para executar essa função. em outras palavras, o SDK do formato de mídia Windows requer uma atualização de segurança.<br/> |



 

## <a name="remarks"></a>Comentários

essa chamada só pode ser feita em um dispositivo que ofereça suporte a Windows mídia DRM 10 para dispositivos portáteis. Você deve especificar pelo menos um parâmetro de limite.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>WMDRMDeviceApp. h (também requer Wmdrmdeviceapp \_ i. c, criado a partir de WMDRMDeviceApp. idl)</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>Mssachlp. lib</dt> </dl>                                                                        |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Lidando com conteúdo protegido no aplicativo**](handling-protected-content-in-the-application.md)
</dt> <dt>

[**Interface IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3)
</dt> <dt>

[**Interface IWMDRMDeviceApp**](iwmdrmdeviceapp.md)
</dt> </dl>

 

 





