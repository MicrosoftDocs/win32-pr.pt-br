---
title: Método IWMDRMLicenseManagement CreateLicenseRevocationChallenge (wmdrmsdk. h)
description: O método CreateLicenseRevocationChallenge gera um desafio de revogação de licença.
ms.assetid: 31fcf7a7-1af8-4474-abac-eddb1070975b
keywords:
- Formato de mídia do Windows do método CreateLicenseRevocationChallenge
- Método CreateLicenseRevocationChallenge Windows Media Format, interface IWMDRMLicenseManagement
- Formato de mídia do Windows de interface IWMDRMLicenseManagement, método CreateLicenseRevocationChallenge
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
ms.openlocfilehash: 3e7fd0acb41b9a2548e5be708611529bea92e131
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105815499"
---
# <a name="iwmdrmlicensemanagementcreatelicenserevocationchallenge-method"></a>Método IWMDRMLicenseManagement:: CreateLicenseRevocationChallenge

O método **CreateLicenseRevocationChallenge** gera um desafio de revogação de licença.

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

*pbMachineID* \[ no\]
</dt> <dd>

Identificador de máquina especificado pelo usuário. Esse valor é usado para consultar uma licença no servidor e deve estar de acordo com qualquer formato que o servidor de licença usa.

</dd> <dt>

*cbMachineID* \[ no\]
</dt> <dd>

Tamanho, em bytes, do identificador da máquina.

</dd> <dt>

*pbChallenge* \[ no\]
</dt> <dd>

Dados de desafio especificados pelo usuário. Esses dados, além do identificador da máquina, são usados para consultar o servidor de licença para que as licenças sejam revogadas.

</dd> <dt>

*cbChallenge* \[ no\]
</dt> <dd>

Tamanho, em bytes, dos dados de desafio.

</dd> <dt>

*ppbChallengeOutput* \[ fora\]
</dt> <dd>

Endereço de um ponteiro que recebe o endereço da saída de desafio. Esse buffer é o dado que é enviado para o serviço de revogação de licença. Quando terminar com esses dados, você deverá liberar a memória chamando **CoTaskMemFree**.

</dd> <dt>

*pcbChallengeOutput* \[ fora\]
</dt> <dd>

Endereço de uma variável que recebe o tamanho dos dados de saída de desafio alocados, em bytes.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

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

 

 





