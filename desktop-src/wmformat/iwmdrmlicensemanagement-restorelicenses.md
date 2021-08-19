---
title: Método IWMDRMLicenseManagement RestoreLicenses (Wmdrmsdk.h)
description: O método RestoreLicenses restaura licenças de um backup de licença criado chamando o método BackupLicenses.
ms.assetid: 83e4b748-0f69-4a9e-b531-047c9a2be1fe
keywords:
- Formato de mídia do windows do método RestoreLicenses
- Formato de mídia do windows do método RestoreLicenses, interface IWMDRMLicenseManagement
- Formato de mídia da interface IWMDRMLicenseManagement , método RestoreLicenses
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.RestoreLicenses
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2a35fdd33df2387bb59dfac64f554dd8b5953fa3015afec6ca643725b9bd58f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117846934"
---
# <a name="iwmdrmlicensemanagementrestorelicenses-method"></a>Método IWMDRMLicenseManagement::RestoreLicenses

O **método RestoreLicenses** restaura licenças de um backup de licença criado chamando o [**método BackupLicenses.**](iwmdrmlicensemanagement-backuplicenses.md)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT RestoreLicenses(
  [in]  BSTR     bstrBackupDirectory,
  [in]  DWORD    dwFlags,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrBackupDirectory* \[ Em\]
</dt> <dd>

Caminho UNC do local do qual as licenças serão restauradas.

</dd> <dt>

*dwFlags* \[ Em\]
</dt> <dd>

Sinalizadores que especificam as opções de restauração a usar. O único sinalizador atualmente com suporte é WMDRM RESTORE INDIVIDUALIZE, que configura o método para executar a individualização como parte da \_ \_ restauração, se necessário.

</dd> <dt>

*ppunkCancelationCookie* \[ out\]
</dt> <dd>

Ponteiro que recebe um ponteiro para a interface **IUnknown** de um objeto que identifica essa chamada assíncrona. Esse ponteiro de interface pode ser usado para cancelar a chamada assíncrona chamando o método [**IWMDRMEventGenerator::CancelAsyncOperation.**](iwmdrmeventgenerator-cancelasyncoperation.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT.** Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

Esse método é executado de forma assíncrona. Ele retorna imediatamente após ser chamado e gera uma série de eventos **MEWMDRMLicenseRestoreProgress** seguidos por um evento **MEWMDRMLicenseRestoreCompleted** quando o processamento é concluído. O valor de cada um dos **eventos MEWMDRMLicenseRestoreProgress obtidos** chamando **IMFMediaEvent::GetValue** é um ponteiro **IUnknown.** Você pode chamar o **método QueryInterface** da interface **IUnknown** recuperada para obter uma instância da interface [**IWMDRMLicenseBackupRestoreStatus.**](iwmdrmlicensebackuprestorestatus.md)

Para obter mais informações sobre como usar os métodos assíncronos das APIs estendidas do cliente drm de Windows mídia, consulte Usando o modelo de evento [Media Foundation .](using-the-media-foundation-model.md)

O backup pode ser do computador local ou de um computador diferente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IWMDRMLicenseManagement Interface**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





