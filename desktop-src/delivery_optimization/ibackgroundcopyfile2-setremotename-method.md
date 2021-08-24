---
title: Método setremotename IBackgroundCopyFile2 (Deliveryoptimization. h)
description: Altera o nome remoto para uma nova URL em um trabalho de download.
ms.assetid: 344D4193-C96E-4B94-AA53-F9307FEB2565
keywords:
- Método setremotename
- Método setremotename, interface IBackgroundCopyFile2
- Interface IBackgroundCopyFile2, método setremotename
topic_type:
- apiref
api_name:
- IBackgroundCopyFile2.SetRemoteName
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e4a2ed93a264aa12d61291c3562a455a026e0dfd0d727648b7d13f6ffe360015
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119636016"
---
# <a name="ibackgroundcopyfile2setremotename-method"></a>Método IBackgroundCopyFile2:: setremotename

Altera o nome remoto para uma nova URL em um trabalho de download.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetRemoteName(
  [in] LPCWSTR RemoteName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Remotoname* \[ no\]
</dt> <dd>

Cadeia de caracteres terminada em nulo que contém o nome do arquivo no servidor. Para obter informações sobre como especificar o nome remoto, consulte o membro **RemoteName** .

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método retorna os seguintes valores de retorno, bem como outros.



| Código de retorno                                                                                  | Descrição                                                                                                           |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl>     | Êxito<br/>                                                                                                    |
| <dl> <dt>**E_INVALIDARG**</dt> </dl> | O novo nome remoto é uma URL inválida ou a nova URL é muito longa (a URL não pode exceder 2.200 caracteres).<br/> |



 

## <a name="remarks"></a>Comentários

Normalmente, você chamará esse método se quiser alterar a URL usada para transferir o arquivo ou se quiser alterar o nome ou o caminho do arquivo.

Esse método não serializa quando retorna. Para serializar a alteração, [**suspenda**](ibackgroundcopyjob-suspend.md) o trabalho, chame esse método (se estiver alterando vários arquivos no trabalho, use um loop) e [**retome**](ibackgroundcopyjob-resume.md) o trabalho. Chamar o método **método ibackgroundcopyjob:: resume** serializa a alteração.

Se o carimbo de data/hora ou o tamanho de arquivo do novo nome remoto for diferente do nome remoto anterior ou o novo servidor não der suporte à retomada do ponto de verificação (para nomes remotos HTTP), o reiniciará o download. Caso contrário, a transferência será retomada da mesma posição no novo servidor. Não reinicia arquivos já transferidos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, \[ somente aplicativos da área de trabalho da versão 1709\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Servidor, versão 1709 \[ aplicativos da área de trabalho\]<br/>                                       |
| Cabeçalho<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyFile2 é definido como 83e81b93-0873-474D-8a8c-f2018b1a939c<br/>             |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IBackgroundCopyFile2**](ibackgroundcopyfile2.md)
</dt> </dl>

 

 





