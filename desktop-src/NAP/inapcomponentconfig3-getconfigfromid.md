---
title: Método GetConfigFromID INapComponentConfig3 (NapCommon.h)
description: É implementado por SHVs (validadores de saúde do sistema) para fornecer uma maneira de obter dados de configuração para uma ID de configuração específica.
ms.assetid: 5c91681d-16d6-42f3-b1e0-c4b6e7561a73
keywords:
- NAP do método GetConfigFromID
- Método GetConfigFromID NAP, interface INapComponentConfig3
- INapComponentConfig3 interface NAP , método GetConfigFromID
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
ms.openlocfilehash: 638704b5706b68b67f854a6a52b6c845be3fb757b596e9f5425f315c7d679fb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118368363"
---
# <a name="inapcomponentconfig3getconfigfromid-method"></a>Método INapComponentConfig3::GetConfigFromID

> [!Note]  
> A plataforma de Proteção de Acesso à Rede não está disponível a partir do Windows 10

 

O **método GetConfigFromID** é implementado por SHVs (validadores de saúde do sistema) para fornecer uma maneira de obter dados de configuração para uma ID de configuração específica.

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

*configID* \[ Em\]
</dt> <dd>

Um valor que representa a configuração. Se *ConfigID* for **0**, o SHV deverá retornar os dados de configuração padrão em *outdata*.

</dd> <dt>

*count* \[ out\]
</dt> <dd>

O tamanho, em bytes, dos dados de configuração retornados em *outdata*.

</dd> <dt>

*outdata* \[ out\]
</dt> <dd>

No retorno, uma matriz BYTE que contém os dados de configuração representados por *ConfigID*.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um dos códigos de erro a seguir com base no resultado dessa operação.



| Código de retorno                                                                                                    | Descrição                             |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                          | A operação teve êxito.<br/> |
| <dl> <dt>**NAP \_ E \_ SHV \_ CONFIG NÃO \_ \_ ENCONTRADO**</dt> </dl> | *ConfigID* não pode ser encontrado.<br/>  |



 

## <a name="remarks"></a>Comentários

O [**método NewConfig**](inapcomponentconfig3-newconfig.md) deve ser usado para alocar dados de configuração para *ConfigID* antes que esse método possa ser chamado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do Server 2008 R2 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>NapCommon.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapCommon.idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**INapComponentConfig3**](inapcomponentconfig3.md)
</dt> </dl>

 

 





