---
title: Método GetConfig INapComponentConfig (NapCommon. h)
description: Recupera a configuração do componente do validador da integridade do sistema (SHV).
ms.assetid: 57a1d3a7-05c0-4e0f-91b8-b3cf8982d04f
keywords:
- Método GetConfig NAP
- Método GetConfig NAP, interface INapComponentConfig
- INapComponentConfig interface NAP, método GetConfig
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
ms.openlocfilehash: e3e07465d768c8902166150e53d4200e775e2597
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455722"
---
# <a name="inapcomponentconfiggetconfig-method"></a>Método INapComponentConfig:: GetConfig

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O método **GetConfig** recupera a configuração do componente do validador da integridade do sistema (SHV).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetConfig(
  [out] UINT16 *bCount,
  [out] BYTE   **data
) const;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bCount* \[ fora\]
</dt> <dd>

O tamanho, em bytes, do blob de configuração de *dados* .

</dd> <dt>

*dados* \[ do fora\]
</dt> <dd>

Um ponteiro para o endereço dos dados de configuração do componente SHV.

> [!Note]  
> Os dados de configuração exportados de um computador x86 usando o método **GetConfig** podem ser importados para um computador x64 usando o método [**setconfig**](inapcomponentconfig-setconfig.md) e vice-versa. Portanto, os dados de configuração devem estar em um formato independente de arquitetura, como XML. Usar XML em vez de um fluxo de bytes torna mais fácil usar dados de configuração em diferentes arquiteturas. Os elementos XML usados nos dados de configuração são determinados pelo implementador.

 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um dos seguintes códigos de erro com base no resultado dessa operação.



| Código de retorno                                                                                     | Descrição                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | A operação teve êxito.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Erro de permissões, acesso negado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | O limite de recursos do sistema não pôde executar a operação.<br/> |



 

## <a name="remarks"></a>Comentários

O parâmetro de dados deve ser alocado pelo receptor (implementador de componente) usando **CoTaskMemAlloc** e liberado pelo chamador usando **CoTaskMemFree**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>NapCommon. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>NapCommon. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**INapComponentConfig**](inapcomponentconfig.md)
</dt> <dt>

[**INapComponentConfig:: setconfig**](inapcomponentconfig-setconfig.md)
</dt> </dl>

 

 





