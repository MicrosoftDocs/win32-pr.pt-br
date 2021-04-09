---
description: Valide um texto de configuração para exatidão sem defini-lo como ativo. Retorna 1 em caso de êxito, 0 em erro.
ms.assetid: baeabed0-7717-498a-9886-e49e4a101711
ms.tgt_platform: multiple
title: Método ValidateConfiguration da classe Control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.ValidateConfiguration
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: d4e1d0061b779a54973aeea1a487d8838781cf6c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920138"
---
# <a name="validateconfiguration-method-of-the-control-class"></a>Método ValidateConfiguration da classe Control

Valide um texto de configuração para exatidão sem defini-lo como ativo. Retorna 1 em caso de êxito, 0 em erro.

## <a name="syntax"></a>Sintaxe


```mof
Uint32 ValidateConfiguration(
  [in]  string Config,
  [out] string ErrorString,
  [out] string WarningString,
  [out] string InfoString,
  [out] uint32 ErrorType
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Configuração* \[ do no\]
</dt> <dd>

A configuração a ser verificada.

</dd> <dt>

*Errostring* \[ fora\]
</dt> <dd>

Quando esse método retornar, se houver um erro, esse parâmetro conterá uma descrição do erro de validação para a operação.

</dd> <dt>

*Aviso de* \[ fora\]
</dt> <dd>

Quando esse método retorna, esse parâmetro contém uma descrição de quaisquer avisos de validação para a operação.

A cadeia de texto com avisos.

</dd> <dt>

*Infostring* \[ fora\]
</dt> <dd>

Quando esse método retorna, esse parâmetro contém um conjunto de informações sobre a configuração.

</dd> <dt>

*ErrorType* \[ fora\]
</dt> <dd>

Quando esse método retornar, se houver um erro de validação, esse parâmetro indicará o tipo de erro.

Os valores possíveis são:

<dt>

0
</dt> <dd>

O argumento está ausente.

</dd> <dt>

1
</dt> <dd>

O formato do argumento é inválido.

</dd> <dt>

2
</dt> <dd>

Um argumento de configuração é inválido.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor retornado

<dl> <dt>


</dt> <dd>

0

Falha

</dd> <dt>


</dt> <dd>

1

Sucesso

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10\]<br/>                                                          |
| Servidor mínimo com suporte<br/> | Windows Server 2016<br/>                                                                       |
| Namespace<br/>                | Raiz \\ do Microsoft \\ Windows \\ BootEventCollector<br/>                                              |
| MOF<br/>                      | <dl> <dt>BootEventCollectorWMI. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>BEvtCol.exe</dt> </dl>               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Control**](control.md)
</dt> </dl>

 

 




