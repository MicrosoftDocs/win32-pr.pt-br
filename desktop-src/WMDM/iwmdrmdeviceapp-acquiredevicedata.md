---
title: Método IWMDRMDeviceApp AcquireDeviceData (WMDRMDeviceApp. h)
description: O método AcquireDeviceData inicializa ou redefine um relógio seguro do dispositivo.
ms.assetid: 2f1cfdb9-0f07-4bee-94aa-b33b039453d0
keywords:
- Método AcquireDeviceData Windows Media Gerenciador de Dispositivos
- Método AcquireDeviceData Windows Media Gerenciador de Dispositivos, interface IWMDRMDeviceApp
- Interface IWMDRMDeviceApp Windows Media Gerenciador de Dispositivos, método AcquireDeviceData
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp.AcquireDeviceData
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 268572e5dad3dffd0fe15956a0ff145f277fb6db
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105770534"
---
# <a name="iwmdrmdeviceappacquiredevicedata-method"></a>Método IWMDRMDeviceApp:: AcquireDeviceData

O método **AcquireDeviceData** inicializa ou redefine um relógio seguro do dispositivo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT AcquireDeviceData(
  [in]  IWMDMDevice    *pDevice,
  [in]  IWMDMProgress3 *pProgressCallback,
  [in]  DWORD          dwFlags,
  [out] DWORD          *pdwStatus
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDevice* \[ no\]
</dt> <dd>

Ponteiro para uma interface [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) para o dispositivo que irá relatar dados de medição.

</dd> <dt>

*pProgressCallback* \[ no\]
</dt> <dd>

O retorno de chamada de progresso por meio do qual o aplicativo pode acompanhar o progresso do evento ou cancelar o evento. O progresso é identificado pelo parâmetro *EventID* dos métodos [**IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3) .

</dd> <dt>

*dwFlags* \[ no\]
</dt> <dd>

Um **or** lógico de um ou ambos os sinalizadores a seguir, especificando a ação a ser executada. Esse valor é recuperado do parâmetro *pdwStatus* de [**IWMDRMDeviceApp:: QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md) ou [**IWMDRMDeviceApp2:: QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md). Você pode usar o sinalizador *pdwStatus* diretamente.



| Sinalizador                        | Descrição                                   |
|-----------------------------|-----------------------------------------------|
| \_NEEDCLOCK de dispositivo WMDRM \_    | Adquira um relógio de um servidor de clock seguro.   |
| \_REFRESHCLOCK de dispositivo WMDRM \_ | Atualize o relógio de um servidor de relógio seguro. |



 

</dd> <dt>

*pdwStatus* \[ fora\]
</dt> <dd>

Um dos valores **DWORD** a seguir que especificam o status retornado pelo dispositivo.



| Status | Descrição                                                     |
|--------|-----------------------------------------------------------------|
| 0      | Não há suporte para a ação.                                    |
| 1      | O relógio de segurança do dispositivo não pôde ser adquirido do serviço. |
| 2      | Não foi possível definir o Clock seguro do dispositivo.                     |
| 3      | O clock de segurança do dispositivo foi definido.                              |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                                                                             | Descrição                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                                    | O método foi bem-sucedido.<br/>                                                                                                    |
| <dl> <dt>**DRM \_ E \_ INVALIDARG**</dt> </dl>                                       | Um ou mais argumentos não são válidos.<br/>                                                                                     |
| <dl> <dt>**dispositivo \_ ns \_ E \_ não \_ WMDRM \_**</dt> </dl>                        | O dispositivo especificado não é um dispositivo compatível com DRM do Windows Media.<br/>                                                       |
| <dl> <dt>**o NS \_ E \_ DRM \_ não consegue \_ obter o \_ \_ \_ Clock seguro**</dt> </dl>               | Falha ao recuperar o desafio de relógio seguro do dispositivo ou não foi possível recuperar a URL do clock seguro do desafio.<br/> |
| <dl> <dt>**o NS \_ E \_ DRM \_ não pode \_ obter o \_ \_ relógio seguro \_ \_ do \_ servidor**</dt> </dl> | Falha ao recuperar a resposta do relógio seguro do servidor do clock seguro.<br/>                                               |
| <dl> <dt>**o NS \_ E \_ DRM \_ não pode \_ definir o \_ \_ \_ relógio seguro**</dt> </dl>               | Falha ao enviar o desafio de relógio seguro para o dispositivo ou o dispositivo não pôde definir o relógio.<br/>                          |



 

## <a name="remarks"></a>Comentários

Este é um método assíncrono; o dispositivo deve aguardar o retorno de chamada [**IWMDMProgress:: End**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmprogress-end) para esta operação antes de tentar reproduzir qualquer conteúdo licenciado.

Um aplicativo pode saber se o dispositivo deve ter seu relógio redefinido ou atualizado chamando [**IWMDRMDeviceApp:: QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md) ou [**IWMDRMDeviceApp2:: QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md).

Seu aplicativo deve ter uma conexão com a Internet para habilitá-lo a adquirir ou redefinir um relógio seguro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>WMDRMDeviceApp. h (também requer Wmdrmdeviceapp \_ i. c, criado a partir de WMDRMDeviceApp. idl)</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>Mssachlp. lib</dt> </dl>                                                                        |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Lidando com conteúdo protegido no aplicativo**](handling-protected-content-in-the-application.md)
</dt> <dt>

[**Interface IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)
</dt> <dt>

[**Interface IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3)
</dt> <dt>

[**Interface IWMDRMDeviceApp**](iwmdrmdeviceapp.md)
</dt> </dl>

 

 





