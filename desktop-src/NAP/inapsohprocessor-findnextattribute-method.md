---
title: Método INapSoHProcessor FindNextAttribute (NapProtocol. h)
description: Localiza o local (índice) do próximo atributo do tipo indicado por SoHAttributeType.
ms.assetid: 0ff94a32-ece8-4a89-9ee9-93c5e14dfb6c
keywords:
- Método FindNextAttribute NAP
- Método FindNextAttribute NAP, interface INapSoHProcessor
- INapSoHProcessor interface NAP, método FindNextAttribute
topic_type:
- apiref
api_name:
- INapSoHProcessor.FindNextAttribute
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1a270e36f8254ed5dbfcd9776cf013f9d10d4a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644330"
---
# <a name="inapsohprocessorfindnextattribute-method"></a>Método INapSoHProcessor:: FindNextAttribute

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O método **INapSoHProcessor:: FindNextAttribute** localiza o local (índice) do próximo atributo do tipo indicado por *SoHAttributeType*.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT FindNextAttribute(
  [in]  UINT16           fromLocation,
  [in]  SoHAttributeType type,
  [out] UINT16           *attributeLocation
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*fromLocation* \[ no\]
</dt> <dd>

O local inicial (índice) no pacote da declaração de integridade (SoH) para iniciar a pesquisa de atributo. Esse valor deve estar no intervalo de 0 a (**numAttrib** -1) em que **numAttrib** é recuperado usando [**INapSoHProcessor:: GetNumberOfAttributes**](inapsohprocessor-getnumberofattributes-method.md).

> [!Note]  
> O pacote SoH usa índices de atributos baseados em 0.

 

</dd> <dt>

*tipo* \[ de no\]
</dt> <dd>

Uma estrutura [**SoHAttributeType**](sohattributetype-enum.md) que contém o tipo de atributo a ser localizado.

</dd> <dt>

*attributeLocation* \[ fora\]
</dt> <dd>

Um ponteiro que contém o local (índice) no pacote SoH do primeiro atributo do tipo *SoHAttributeType* do índice *fromLocation*.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Outros códigos de erro específicos de COM também podem ser retornados.



| Código de retorno                                                                                            | Descrição                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Operação bem-sucedida.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>        | Erro de permissões, acesso negado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>         | O limite de recursos do sistema não pôde executar a operação.<br/> |
| <dl> <dt>**arquivo de erro \_ \_ não \_ encontrado**</dt> </dl> | Atributo não encontrado.<br/>                                    |



 

## <a name="remarks"></a>Comentários

O método **FindNextAttribute** procura atributos do tipo *SoHAttributeType* a partir do índice especificado por *fromLocation* e superior até que uma correspondência seja encontrada. Se nenhuma correspondência for encontrada, **o \_ arquivo de erro \_ não \_ encontrado** será retornado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                       |
| parâmetro<br/>                   | <dl> <dt>NapProtocol. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>NapProtocol. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**INapSoHProcessor**](inapsohprocessor.md)
</dt> </dl>

 

 





