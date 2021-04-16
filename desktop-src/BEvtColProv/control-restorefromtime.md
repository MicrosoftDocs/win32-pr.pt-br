---
description: Restaure a configuração ativa do coletor de um arquivo de backup, selecionado por um carimbo de data/hora.
ms.assetid: 3ee4156b-c68f-4c44-b9be-dd86e8f4b340
ms.tgt_platform: multiple
title: Método RestoreFromTime da classe Control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.RestoreFromTime
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 79b89c0c89e4954d8a641d037e08757f83cad618
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105747710"
---
# <a name="restorefromtime-method-of-the-control-class"></a>Método RestoreFromTime da classe Control

Restaure a configuração ativa do coletor de um arquivo de backup, selecionado por um carimbo de data/hora.

## <a name="syntax"></a>Sintaxe


```mof
Uint32 RestoreFromTime(
  [in]  Uint32 TargetTimestampLow,
  [in]  Uint32 TargetTimestampHigh,
  [in]  Uint32 OldTimestampLow,
  [in]  Uint32 OldTimestampHigh,
  [out] Uint32 NewTimestampLow,
  [out] Uint32 NewTimestampHigh,
  [out] Uint32 OriginalTimestampLow,
  [out] Uint32 OriginalTimestampHigh,
  [out] string ErrorString,
  [out] string WarningString,
  [out] string InfoString,
  [out] uint32 ErrorType
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*TargetTimestampLow* \[ no\]
</dt> <dd>

Restaure para o arquivo de backup neste carimbo de data/hora. Essa é a parte inferior do [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*TargetTimestampHigh* \[ no\]
</dt> <dd>

Restaure para o arquivo de backup neste carimbo de data/hora. Essa é a parte superior do [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*OldTimestampLow* \[ no\]
</dt> <dd>

O carimbo de data/hora de quando a configuração anterior foi definida. Se não for 0, habilita a verificação de atomicidade: a nova configuração será aplicada somente se o carimbo de data/hora da configuração antiga for correspondente (ou seja, a configuração não foi alterada entre elas). Essa é a parte inferior do [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*OldTimestampHigh* \[ no\]
</dt> <dd>

O carimbo de data/hora de quando a configuração anterior foi definida. Se não for 0, habilita a verificação de atomicidade: a nova configuração será aplicada somente se o carimbo de data/hora da configuração antiga for correspondente (ou seja, a configuração não foi alterada entre elas). Essa é a parte superior do [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*NewTimestampLow* \[ fora\]
</dt> <dd>

O carimbo de data/hora de quando a nova configuração foi definida, se a chamada tiver êxito. Essa é a parte inferior do [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*NewTimestampHigh* \[ fora\]
</dt> <dd>

O carimbo de data/hora de quando a nova configuração foi definida, se a chamada tiver êxito. Essa é a parte superior do [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*OriginalTimestampLow* \[ fora\]
</dt> <dd>

O carimbo de data/hora original de quando a configuração restaurada foi definida pela primeira vez. Essa é a parte inferior do [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*OriginalTimestampHigh* \[ fora\]
</dt> <dd>

O carimbo de data/hora original de quando a configuração restaurada foi definida pela primeira vez. Essa é a parte superior do [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

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

O tipo do erro: Observe que 0 ou ausente indica êxito.

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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10\]<br/>                                                          |
| Servidor mínimo com suporte<br/> | Windows Server 2016<br/>                                                                       |
| Namespace<br/>                | Raiz \\ do Microsoft \\ Windows \\ BootEventCollector<br/>                                              |
| MOF<br/>                      | <dl> <dt>BootEventCollectorWMI. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>BEvtCol.exe</dt> </dl>               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Controlo**](control.md)
</dt> </dl>

 

