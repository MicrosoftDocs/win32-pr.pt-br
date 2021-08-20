---
title: Método GetConfig INapComponentConfig (NapCommon.h)
description: Recupera a configuração de componente do SHV (validador de saúde do sistema).
ms.assetid: 57a1d3a7-05c0-4e0f-91b8-b3cf8982d04f
keywords:
- NAP do método GetConfig
- Método GetConfig NAP, interface INapComponentConfig
- Interface INapComponentConfig NAP, método GetConfig
topic_type:
- apiref
api_name:
- INapComponentConfig.GetConfig
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8dc5495df10e3a5ff3907941644c5558aea35d29b52c8773fb56314c4a8620c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118134494"
---
# <a name="inapcomponentconfiggetconfig-method"></a>Método INapComponentConfig::GetConfig

> [!Note]  
> A plataforma de Proteção de Acesso à Rede não está disponível a partir do Windows 10

 

O **método GetConfig** recupera a configuração do componente SHV (validador de saúde do sistema).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetConfig(
  [out] UINT16 *bCount,
  [out] BYTE   **data
) const;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bCount* \[ out\]
</dt> <dd>

O tamanho, em bytes, do blob *de configuração* de dados.

</dd> <dt>

*dados* \[ out\]
</dt> <dd>

Um ponteiro para o endereço dos dados de configuração do componente SHV.

> [!Note]  
> Os dados de configuração exportados de um computador x86 usando o **método GetConfig** podem ser importados para um computador x64 usando o [**método SetConfig**](inapcomponentconfig-setconfig.md) e vice-versa. Portanto, os dados de configuração devem estar em um formato de arquitetura, como XML. Usar XML em vez de um fluxo de byte facilita o uso de dados de configuração em arquiteturas diferentes. Os elementos XML usados nos dados de configuração são determinados pelo implementador.

 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um dos códigos de erro a seguir com base no resultado dessa operação.



| Código de retorno                                                                                     | Descrição                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | A operação teve êxito.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Erro de permissões, acesso negado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite de recursos do sistema, não foi possível executar a operação.<br/> |



 

## <a name="remarks"></a>Comentários

O parâmetro de dados deve ser alocado pelo chamador (implementador de componente) usando **CoTaskMemAlloc** e liberado pelo chamador usando **CoTaskMemFree.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                     |
| Cabeçalho<br/>                   | <dl> <dt>NapCommon.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapCommon.idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**INapComponentConfig**](inapcomponentconfig.md)
</dt> <dt>

[**INapComponentConfig::SetConfig**](inapcomponentconfig-setconfig.md)
</dt> </dl>

 

 





