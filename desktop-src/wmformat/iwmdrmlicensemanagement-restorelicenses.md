---
title: Método IWMDRMLicenseManagement RestoreLicenses (wmdrmsdk. h)
description: O método RestoreLicenses restaura licenças de um backup de licença que foi criado chamando o método BackupLicenses.
ms.assetid: 83e4b748-0f69-4a9e-b531-047c9a2be1fe
keywords:
- Formato de mídia do Windows do método RestoreLicenses
- Método RestoreLicenses Windows Media Format, interface IWMDRMLicenseManagement
- Formato de mídia do Windows de interface IWMDRMLicenseManagement, método RestoreLicenses
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
ms.openlocfilehash: fb07f3989ff19faa723e4b1d1cd50dc4e269f219
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105765035"
---
# <a name="iwmdrmlicensemanagementrestorelicenses-method"></a>Método IWMDRMLicenseManagement:: RestoreLicenses

O método **RestoreLicenses** restaura licenças de um backup de licença que foi criado chamando o método [**BackupLicenses**](iwmdrmlicensemanagement-backuplicenses.md) .

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

*bstrBackupDirectory* \[ no\]
</dt> <dd>

Caminho UNC do local do qual as licenças serão restauradas.

</dd> <dt>

*dwFlags* \[ no\]
</dt> <dd>

Sinalizadores que especificam as opções de restauração a serem usadas. O único sinalizador com suporte no momento é o WMDRM \_ Restore \_ individual, que configura o método para executar individualização como parte da restauração, se necessário.

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

Esse método é executado de forma assíncrona. Ele retorna imediatamente depois de ser chamado e, em seguida, gera uma série de eventos **MEWMDRMLicenseRestoreProgress** seguidos por um evento **MEWMDRMLicenseRestoreCompleted** quando o processamento é concluído. O valor de cada um dos eventos **MEWMDRMLicenseRestoreProgress** obtidos chamando **IMFMediaEvent:: GetValue** é um ponteiro **IUnknown** . Você pode chamar o método **QueryInterface** da interface **IUnknown** recuperada para obter uma instância da interface [**IWMDRMLicenseBackupRestoreStatus**](iwmdrmlicensebackuprestorestatus.md) .

Para obter mais informações sobre como usar os métodos assíncronos das APIs estendidas do cliente DRM do Windows Media, consulte [usando o modelo de evento Media Foundation](using-the-media-foundation-model.md).

O backup pode ser do computador local ou de um computador diferente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





