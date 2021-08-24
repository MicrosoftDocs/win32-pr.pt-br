---
description: Se a configuração atual for um resultado da função desfazer/refazer/restaurar, o marcará como se ela estivesse definida explicitamente, de modo que o histórico preservará a hora em que foi definido e um arquivo de backup será criado para ele na próxima alteração de configuração.
ms.assetid: 1b3d398a-c7f9-4e21-9e43-1245a13fe564
ms.tgt_platform: multiple
title: Método Checkpoint da classe Control (Srrestoreptapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.Checkpoint
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: ff71086703e409331e420fd064f73ff2406ec4e5167ea97da78b2afc498bf244
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119579846"
---
# <a name="checkpoint-method-of-the-control-class"></a>Método Checkpoint da classe Control

Se a configuração atual for um resultado da função desfazer/refazer/restaurar, o marcará como se ela estivesse definida explicitamente, de modo que o histórico preservará a hora em que foi definido e um arquivo de backup será criado para ele na próxima alteração de configuração. Se a configuração atual já foi definida explicitamente, não terá efeito.

## <a name="syntax"></a>Sintaxe


```mof
Uint32 Checkpoint(
  [in]  Uint32 OldTimestampLow,
  [in]  Uint32 OldTimestampHigh,
  [out] string ErrorString,
  [out] string WarningString,
  [out] string InfoString,
  [out] uint32 ErrorType
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*OldTimestampLow* \[ no\]
</dt> <dd>

O carimbo de data/hora de quando a configuração atual foi definida. Se não for 0, habilitará a verificação de atomicidade: a ação será aplicada somente se o carimbo de data/hora da configuração antiga for correspondente (ou seja, a configuração não foi alterada entre elas). Essa é a parte inferior do [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*OldTimestampHigh* \[ no\]
</dt> <dd>

O carimbo de data/hora de quando a configuração atual foi definida. Se não for 0, habilitará a verificação de atomicidade: a ação será aplicada somente se o carimbo de data/hora da configuração antiga for correspondente (ou seja, a configuração não foi alterada entre elas). Essa é a parte superior do [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*Errostring* \[ fora\]
</dt> <dd>

A cadeia de texto com a explicação do erro.

</dd> <dt>

*Aviso de* \[ fora\]
</dt> <dd>

A cadeia de texto com avisos.

</dd> <dt>

*Infostring* \[ fora\]
</dt> <dd>

A cadeia de texto com informações sobre a configuração.

</dd> <dt>

*ErrorType* \[ fora\]
</dt> <dd>

O tipo do erro. Observe que 0 ou ausente indicam êxito.

<dt>

0
</dt> <dd>

Sucesso.

</dd> <dt>

1
</dt> <dd>

formato de argumento inadequado

</dd> <dt>

2
</dt> <dd>

valor de argumento inadequado

</dd> <dt>

3
</dt> <dd>

erro ao abrir o recurso (soquete)

</dd> <dt>

4
</dt> <dd>

erro de persistência (gravação de arquivo)

</dd> <dt>

5
</dt> <dd>

erro de atomicidade (o carimbo de data/hora antigo não corresponde)

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
| Cliente mínimo com suporte<br/> | Windows 10 \[ somente aplicativos da área de trabalho\]<br/>                                                          |
| Servidor mínimo com suporte<br/> | Windows Server 2016<br/>                                                                       |
| Namespace<br/>                | raiz \\ do Microsoft \\ Windows \\ BootEventCollector<br/>                                              |
| Cabeçalho<br/>                   | <dl> <dt>Srrestoreptapi. h</dt> </dl>          |
| MOF<br/>                      | <dl> <dt>BootEventCollectorWMI. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>BEvtCol.exe</dt> </dl>               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Control**](control.md)
</dt> </dl>

 

