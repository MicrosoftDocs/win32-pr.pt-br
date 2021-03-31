---
title: Método INapComponentConfig3 GetConfigFromID (NapCommon. h)
description: É implementado por SHVs (validadores da integridade do sistema) para fornecer uma maneira de obter dados de configuração para uma ID de configuração específica.
ms.assetid: 5c91681d-16d6-42f3-b1e0-c4b6e7561a73
keywords:
- Método GetConfigFromID NAP
- Método GetConfigFromID NAP, interface INapComponentConfig3
- INapComponentConfig3 interface NAP, método GetConfigFromID
topic_type:
- apiref
api_name:
- INapComponentConfig3.GetConfigFromID
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ce3a0e20f19c73271cdcba4070972649fe25aea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644509"
---
# <a name="inapcomponentconfig3getconfigfromid-method"></a>Método INapComponentConfig3:: GetConfigFromID

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O método **GetConfigFromID** é implementado por SHVs (validadores da integridade do sistema) para fornecer uma maneira de obter dados de configuração para uma ID de configuração específica.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetConfigFromID(
  [in]  UINT32 configID,
  [out] UINT16 *count,
  [out] BYTE   **outdata
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*configid* \[ no\]
</dt> <dd>

Um valor que representa a configuração. Se *configid* for **0**, o SHV deverá retornar os dados de configuração padrão em *OutData*.

</dd> <dt>

*contagem* \[ de fora\]
</dt> <dd>

O tamanho, em bytes, dos dados de configuração retornados em *OutData*.

</dd> <dt>

*OutData* \[ fora\]
</dt> <dd>

No retorno, uma matriz de bytes que contém os dados de configuração representados por *configid*.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um dos seguintes códigos de erro com base no resultado dessa operação.



| Código de retorno                                                                                                    | Description                             |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                          | A operação teve êxito.<br/> |
| <dl> <dt>**configuração de NAP \_ E \_ SHV \_ \_ não \_ encontrada**</dt> </dl> | Não foi possível encontrar *configid* .<br/>  |



 

## <a name="remarks"></a>Comentários

O método [**newconfig**](inapcomponentconfig3-newconfig.md) deve ser usado para alocar dados de configuração para *configid* antes que este método possa ser chamado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>NapCommon. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>NapCommon. idl</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**INapComponentConfig3**](inapcomponentconfig3.md)
</dt> </dl>

 

 





