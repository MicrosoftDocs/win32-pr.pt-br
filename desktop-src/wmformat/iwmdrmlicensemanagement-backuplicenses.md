---
title: Método IWMDRMLicenseManagement BackupLicenses (wmdrmsdk. h)
description: O método BackupLicenses cria um backup das licenças no repositório de licenças local.
ms.assetid: f265254d-b240-4a9f-9c67-de9c92e8a14d
keywords:
- Formato de mídia do Windows do método BackupLicenses
- Método BackupLicenses Windows Media Format, interface IWMDRMLicenseManagement
- Formato de mídia do Windows de interface IWMDRMLicenseManagement, método BackupLicenses
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
ms.openlocfilehash: 61c7f676b532353c839a428571f6d28540851bee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105798176"
---
# <a name="iwmdrmlicensemanagementbackuplicenses-method"></a>Método IWMDRMLicenseManagement:: BackupLicenses

O método **BackupLicenses** cria um backup das licenças no repositório de licenças local.

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

*bstrBackupDirectory* \[ no\]
</dt> <dd>

Caminho UNC do local para o qual será feito o backup das licenças.

</dd> <dt>

*dwFlags* \[ no\]
</dt> <dd>

Sinalizadores que especificam as opções de backup a serem usadas. O único sinalizador com suporte no momento é a \_ substituição de backup do WMDRM \_ , que configura o método para substituir os arquivos de backup existentes no diretório.

</dd> <dt>

*ppunkCancelationCookie* \[ fora\]
</dt> <dd>

Ponteiro que recebe um ponteiro para a interface **IUnknown** de um objeto que identifica essa chamada assíncrona. Esse ponteiro de interface pode ser usado para cancelar a chamada assíncrona chamando o método [**IWMDRMEventGenerator:: CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

Esse método é executado de forma assíncrona. Ele retorna imediatamente depois de ser chamado e, em seguida, gera uma série de eventos **MEWMDRMLicenseBackupProgress** seguidos por um evento **MEWMDRMLicenseBackupCompleted** quando o processamento é concluído. O valor de cada um dos eventos **MEWMDRMLicenseBackupProgress** obtidos chamando **IMFMediaEvent:: GetValue** é um ponteiro **IUnknown** . Você pode chamar o método **QueryInterface** da interface **IUnknown** recuperada para obter uma instância da interface [**IWMDRMLicenseBackupRestoreStatus**](iwmdrmlicensebackuprestorestatus.md) .

Para obter mais informações sobre como usar os métodos assíncronos das APIs estendidas do cliente DRM do Windows Media, consulte [usando o modelo de evento Media Foundation](using-the-media-foundation-model.md).

Nem todas as licenças têm permissão para fazer backup. Esse método faz backup apenas de licenças que o permitem.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





