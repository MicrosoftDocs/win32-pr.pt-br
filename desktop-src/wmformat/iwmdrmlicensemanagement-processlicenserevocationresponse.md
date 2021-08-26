---
title: Método IWMDRMLicenseManagement ProcessLicenseRevocationResponse (wmdrmsdk. h)
description: O método ProcessLicenseRevocationResponse revoga licenças do armazenamento de licença local. Esse método usa um LRB (blob de revogação de licença) recebido de um servidor de revogação de licença para identificar as licenças a serem revogadas.
ms.assetid: 4428ac44-c3f4-404e-9997-cbc7360faedf
keywords:
- Formato de mídia do Windows do método ProcessLicenseRevocationResponse
- Método ProcessLicenseRevocationResponse Windows Media Format, interface IWMDRMLicenseManagement
- Formato de mídia do Windows de interface IWMDRMLicenseManagement, método ProcessLicenseRevocationResponse
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.ProcessLicenseRevocationResponse
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d58c33f79db575dec37d7d2ac51e3c65b10416b9ca35a50084f36a56693854be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930306"
---
# <a name="iwmdrmlicensemanagementprocesslicenserevocationresponse-method"></a>IWMDRMLicenseManagement: método rocessLicenseRevocationResponse de:P

O método **ProcessLicenseRevocationResponse** revoga licenças do armazenamento de licença local. Esse método usa um LRB (blob de revogação de licença) recebido de um servidor de revogação de licença para identificar as licenças a serem revogadas.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ProcessLicenseRevocationResponse(
  [in]  BYTE  *pbSignedLRB,
  [in]  DWORD cbSignedLRB,
  [out] BYTE  **ppbSignedACK,
  [out] DWORD *pcbSignedACK
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pbSignedLRB* \[ no\]
</dt> <dd>

Blob de revogação de licença (LRB) recebido do servidor de revogação de licença em resposta a um desafio que foi gerado chamando o método [**CreateLicenseRevocationChallenge**](iwmdrmlicensemanagement-createlicenserevocationchallenge.md) .

</dd> <dt>

*cbSignedLRB* \[ no\]
</dt> <dd>

Tamanho do LRB em bytes.

</dd> <dt>

*ppbSignedACK* \[ fora\]
</dt> <dd>

Endereço de um ponteiro que recebe o endereço da confirmação de revogação de licença. A confirmação deve ser enviada para o serviço de revogação de licença. Quando terminar com esses dados, você deverá liberar a memória chamando **CoTaskMemFree**.

</dd> <dt>

*pcbSignedACK* \[ fora\]
</dt> <dd>

Endereço de uma variável que recebe o tamanho da confirmação em bytes.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

Nenhum.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





