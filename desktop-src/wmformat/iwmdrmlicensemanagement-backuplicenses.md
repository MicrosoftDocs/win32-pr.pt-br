---
title: Método IWMDRMLicenseManagement BackupLicenses (Wmdrmsdk.h)
description: O método BackupLicenses cria um backup das licenças no armazenamento de licenças local.
ms.assetid: f265254d-b240-4a9f-9c67-de9c92e8a14d
keywords:
- Formato de mídia do windows do método BackupLicenses
- Formato de mídia do windows do método BackupLicenses, interface IWMDRMLicenseManagement
- Formato de mídia da interface IWMDRMLicenseManagement , método BackupLicenses
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.BackupLicenses
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3905f8fd464645f7fcd22551360e6a9610913eeea7f191d7e770e24f5ea8cd49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027644"
---
# <a name="iwmdrmlicensemanagementbackuplicenses-method"></a>Método IWMDRMLicenseManagement::BackupLicenses

O **método BackupLicenses** cria um backup das licenças no armazenamento de licenças local.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT BackupLicenses(
  [in]  BSTR     bstrBackupDirectory,
  [in]  DWORD    dwFlags,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrBackupDirectory* \[ Em\]
</dt> <dd>

Caminho UNC do local para o qual as licenças terão o backup feito.

</dd> <dt>

*dwFlags* \[ Em\]
</dt> <dd>

Sinalizadores que especificam as opções de backup a usar. O único sinalizador com suporte no momento é WMDRM BACKUP OVERWRITE, que configura o método para substituir todos os arquivos de \_ \_ backup existentes no diretório.

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

Esse método é executado de forma assíncrona. Ele retorna imediatamente após ser chamado e gera uma série de eventos **MEWMDRMLicenseBackupProgress** seguidos por um evento **MEWMDRMLicenseBackupCompleted** quando o processamento é concluído. O valor de cada um dos **eventos MEWMDRMLicenseBackupProgress obtidos** chamando **IMFMediaEvent::GetValue** é um ponteiro **IUnknown.** Você pode chamar o **método QueryInterface** da interface **IUnknown** recuperada para obter uma instância da interface [**IWMDRMLicenseBackupRestoreStatus.**](iwmdrmlicensebackuprestorestatus.md)

Para obter mais informações sobre como usar os métodos assíncronos das APIs estendidas do cliente drm de Windows mídia, consulte Usando o modelo de evento [Media Foundation .](using-the-media-foundation-model.md)

Nem todas as licenças têm permissão para fazer backup. Esse método só faz o back-up de licenças que o permitem.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IWMDRMLicenseManagement Interface**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





