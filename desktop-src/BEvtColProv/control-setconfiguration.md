---
description: Defina a nova configuração ativa do coletor.
ms.assetid: 1979e657-a8f3-4eab-991c-a884bde10724
ms.tgt_platform: multiple
title: Método SetConfiguration da classe Control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.SetConfiguration
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 4f482de9c4cd8f410371da51e605762a1f92e104
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646220"
---
# <a name="setconfiguration-method-of-the-control-class"></a>Método SetConfiguration da classe Control

Defina a nova configuração ativa do coletor.

## <a name="syntax"></a>Sintaxe


```mof
Uint32 SetConfiguration(
  [in]  string Config,
  [in]  Uint32 OldTimestampLow,
  [in]  Uint32 OldTimestampHigh,
  [out] Uint32 NewTimestampLow,
  [out] Uint32 NewTimestampHigh,
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

A configuração a ser ativada.

</dd> <dt>

*OldTimestampLow* \[ no\]
</dt> <dd>

Os bits de ordem inferior de um carimbo de data/hora que indica quando a configuração ativa atual foi definida. A verificação de atomicidade estará habilitada se essa propriedade não estiver definida como 0.

</dd> <dt>

*OldTimestampHigh* \[ no\]
</dt> <dd>

Os bits de ordem superior de um carimbo de data/hora que indica quando a configuração ativa atual foi definida. A verificação de atomicidade estará habilitada se essa propriedade não estiver definida como 0.

</dd> <dt>

*NewTimestampLow* \[ fora\]
</dt> <dd>

Quando esse método retorna, esse parâmetro contém os bits de ordem inferior de um carimbo de data/hora que indica quando a nova configuração foi definida. A verificação de atomicidade estará habilitada se essa propriedade não estiver definida como 0.

</dd> <dt>

*NewTimestampHigh* \[ fora\]
</dt> <dd>

Quando esse método retorna, esse parâmetro contém os bits de ordem superior do carimbo de data/hora que indica quando a nova configuração foi definida. A verificação de atomicidade estará habilitada se essa propriedade não estiver definida como 0.

</dd> <dt>

*Errostring* \[ fora\]
</dt> <dd>

Quando esse método retornar, se houver um erro, esse parâmetro conterá a descrição do erro.

</dd> <dt>

*Aviso de* \[ fora\]
</dt> <dd>

Quando esse método retornar, esse parâmetro conterá quaisquer mensagens de avisos para a operação.

</dd> <dt>

*Infostring* \[ fora\]
</dt> <dd>

Quando esse método retorna, esse parâmetro contém informações para a nova configuração ativa.

</dd> <dt>

*ErrorType* \[ fora\]
</dt> <dd>

Quando esse método retornar, se houver um erro, esse parâmetro indicará o tipo de erro.

<dt>

0
</dt> <dd>

A nova configuração está ausente.

</dd> <dt>

1
</dt> <dd>

O formato da nova configuração é inválido.

</dd> <dt>

2
</dt> <dd>

A nova configuração é inválida.

</dd> <dt>

3
</dt> <dd>

Ocorreu um erro causado por um Soquete aberto.

</dd> <dt>

4
</dt> <dd>

Houve um erro de gravação de arquivo.

</dd> <dt>

5
</dt> <dd>

Ocorreu um erro de atomicidade.

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

 

 




