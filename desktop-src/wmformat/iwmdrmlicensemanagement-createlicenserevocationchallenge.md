---
title: Método IWMDRMLicenseManagement CreateLicenseRevocationChallenge (Wmdrmsdk.h)
description: O método CreateLicenseRevocationChallenge gera um desafio de revogação de licença.
ms.assetid: 31fcf7a7-1af8-4474-abac-eddb1070975b
keywords:
- Formato de mídia do windows do método CreateLicenseRevocationChallenge
- O método CreateLicenseRevocationChallenge windows Formato de Mídia , interface IWMDRMLicenseManagement
- Formato de mídia da interface IWMDRMLicenseManagement , método CreateLicenseRevocationChallenge
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.CreateLicenseRevocationChallenge
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 851233229d7dde113cf21cfb38419067679843b34ae59ece0e32e326c2a91c46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117846945"
---
# <a name="iwmdrmlicensemanagementcreatelicenserevocationchallenge-method"></a>Método IWMDRMLicenseManagement::CreateLicenseRevocationChallenge

O **método CreateLicenseRevocationChallenge** gera um desafio de revogação de licença.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CreateLicenseRevocationChallenge(
  [in]  BYTE  *pbMachineID,
  [in]  DWORD cbMachineID,
  [in]  BYTE  *pbChallenge,
  [in]  DWORD cbChallenge,
  [out] BYTE  **ppbChallengeOutput,
  [out] DWORD *pcbChallengeOutput
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pbMachineID* \[ Em\]
</dt> <dd>

Identificador de computador especificado pelo usuário. Esse valor é usado para consultar uma licença no servidor e deve estar em conformidade com qualquer formato usado pelo servidor de licença.

</dd> <dt>

*cbMachineID* \[ Em\]
</dt> <dd>

Tamanho, em bytes, do identificador do computador.

</dd> <dt>

*pbChallenge* \[ Em\]
</dt> <dd>

Dados de desafio especificados pelo usuário. Esses dados, além do identificador do computador, são usados para consultar o servidor de licença para que as licenças sejam revogadas.

</dd> <dt>

*cbChallenge* \[ Em\]
</dt> <dd>

Tamanho, em bytes, dos dados de desafio.

</dd> <dt>

*ppbChallengeOutput* \[ out\]
</dt> <dd>

Endereço de um ponteiro que recebe o endereço da saída do desafio. Esse buffer são os dados que são enviados para o serviço de revogação de licença. Quando terminar com esses dados, você deverá liberar a memória chamando **CoTaskMemFree.**

</dd> <dt>

*pcbChallengeOutput* \[ out\]
</dt> <dd>

Endereço de uma variável que recebe o tamanho dos dados de saída de desafio alocados, em bytes.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT.** Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

Nenhum.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IWMDRMLicenseManagement Interface**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





