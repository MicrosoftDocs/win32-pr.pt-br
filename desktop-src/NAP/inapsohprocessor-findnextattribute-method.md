---
title: Método FindNextAttribute de INapSoHProcessor (NapProtocol.h)
description: Localiza o local (índice) do próximo atributo do tipo indicado por SoHAttributeType.
ms.assetid: 0ff94a32-ece8-4a89-9ee9-93c5e14dfb6c
keywords:
- Nap do método FindNextAttribute
- FindNextAttribute method NAP , interface INapSoHProcessor
- INapSoHProcessor interface NAP , método FindNextAttribute
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
ms.openlocfilehash: 4425707487994904d1bd2a622cd1ab66f286469c93e80a8eb01e71c0319426ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118939573"
---
# <a name="inapsohprocessorfindnextattribute-method"></a>Método INapSoHProcessor::FindNextAttribute

> [!Note]  
> A plataforma de Proteção de Acesso à Rede não está disponível a partir do Windows 10

 

O **método INapSoHProcessor::FindNextAttribute** localiza o local (índice) do próximo atributo do tipo indicado por *SoHAttributeType*.

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

*fromLocation* \[ Em\]
</dt> <dd>

O local inicial (índice) no pacote SoH (Instrução de Saúde) para iniciar a pesquisa de atributo. Esse valor deve estar no intervalo de 0 a (**numAttrib** - 1) em que **numAttrib** é recuperado usando [**INapSoHProcessor::GetNumberOfAttributes**](inapsohprocessor-getnumberofattributes-method.md).

> [!Note]  
> O pacote SoH usa índices de atributo baseados em 0.

 

</dd> <dt>

*tipo* \[ Em\]
</dt> <dd>

Uma [**estrutura SoHAttributeType**](sohattributetype-enum.md) que contém o tipo de atributo a ser localizado.

</dd> <dt>

*attributeLocation* \[ out\]
</dt> <dd>

Um ponteiro que contém o local (índice) no pacote SoH do primeiro atributo do tipo *SoHAttributeType* do *índice fromLocation*.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Outros códigos de erro específicos do COM também podem ser retornados.



| Código de retorno                                                                                            | Descrição                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Êxito na operação.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>        | Erro de permissões, acesso negado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>         | Limite de recursos do sistema, não foi possível executar a operação.<br/> |
| <dl> <dt>**ARQUIVO \_ DE ERRO NÃO \_ \_ ENCONTRADO**</dt> </dl> | Atributo não encontrado.<br/>                                    |



 

## <a name="remarks"></a>Comentários

O **método FindNextAttribute** procura atributos do tipo *SoHAttributeType* do índice especificado por *fromLocation* e superior até que uma combinação seja encontrada. Se nenhuma corresponder for encontrada, **ERROR \_ FILE NOT \_ \_ FOUND** será retornado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                       |
| Cabeçalho<br/>                   | <dl> <dt>NapProtocol.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapProtocol.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**INapSoHProcessor**](inapsohprocessor.md)
</dt> </dl>

 

 





