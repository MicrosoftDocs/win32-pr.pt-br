---
description: Restaure a configuração ativa do coletor do arquivo de backup anterior (determinado voltando do timestamp original atual).
ms.assetid: 150fa554-9efd-483e-a177-5fc7766a6a6c
ms.tgt_platform: multiple
title: Método Undo da classe Control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.Undo
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: e46649473da31fac09c65fcecaf44e91eba049c7ddce089d7f3c5ba9de2f8e19
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589036"
---
# <a name="undo-method-of-the-control-class"></a>Método Undo da classe Control

Restaure a configuração ativa do coletor do arquivo de backup anterior (determinado voltando do timestamp original atual). Se a configuração tiver sido definida, isso significa desfazer essa alteração. As chamadas consecutivas serão desfazer para as configurações anteriores e anteriores. Retorna 1 em caso de êxito, 0 em caso de erro.

## <a name="syntax"></a>Sintaxe


```mof
Uint32 Undo(
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

*OldTimestampLow* \[ Em\]
</dt> <dd>

O timestamp de quando a configuração anterior foi definida. Se não for 0, habilita a verificação de atomicidade: a nova configuração será aplicada somente se o timestamp da configuração antiga corresponde (ou seja, a configuração não foi alterada entre elas). Essa é a parte baixa de [**FILETIME.**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)

</dd> <dt>

*OldTimestampHigh* \[ Em\]
</dt> <dd>

O timestamp de quando a configuração anterior foi definida. Se não for 0, habilita a verificação de atomicidade: a nova configuração será aplicada somente se o timestamp da configuração antiga corresponde (ou seja, a configuração não foi alterada entre elas). Essa é a parte alta do [**FILETIME.**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)

</dd> <dt>

*NewTimestampLow* \[ out\]
</dt> <dd>

O timestamp de quando a nova configuração foi definida, se a chamada for bem-sucedida. Essa é a parte baixa de [**FILETIME.**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)

</dd> <dt>

*NewTimestampHigh* \[ out\]
</dt> <dd>

O timestamp de quando a nova configuração foi definida, se a chamada for bem-sucedida. Essa é a parte alta do [**FILETIME.**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)

</dd> <dt>

*OriginalTimestampLow* \[ out\]
</dt> <dd>

O data/hora original de quando a configuração restaurada foi definida pela primeira vez. Essa é a parte baixa de [**FILETIME.**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)

</dd> <dt>

*OriginalTimestampHigh* \[ out\]
</dt> <dd>

O data/hora original de quando a configuração restaurada foi definida pela primeira vez. Essa é a parte alta do [**FILETIME.**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)

</dd> <dt>

*ErrorString* \[ out\]
</dt> <dd>

A cadeia de caracteres de texto com explicação do erro.

</dd> <dt>

*WarningString* \[ out\]
</dt> <dd>

A cadeia de caracteres de texto com avisos.

</dd> <dt>

*InfoString* \[ out\]
</dt> <dd>

A cadeia de caracteres de texto com informações sobre a configuração.

</dd> <dt>

*ErrorType* \[ out\]
</dt> <dd>

O tipo do erro: observe que 0 ou ausente indica êxito.

<dt>

0
</dt> <dd>

Sucesso.

</dd> <dt>

1
</dt> <dd>

formato de argumento ruim

</dd> <dt>

2
</dt> <dd>

valor do argumento ruim

</dd> <dt>

3
</dt> <dd>

erro de abertura de recurso (soquete)

</dd> <dt>

4
</dt> <dd>

erro de persistência (gravação de arquivo)

</dd> <dt>

5
</dt> <dd>

Erro de atomicidade (o antigo timestamp não foi corresponder)

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
| Cliente mínimo com suporte<br/> | \[Windows 10 somente aplicativos da área de trabalho\]<br/>                                                          |
| Servidor mínimo com suporte<br/> | Windows Server 2016<br/>                                                                       |
| Namespace<br/>                | Root \\ Microsoft \\ Windows \\ BootEventCollector<br/>                                              |
| MOF<br/>                      | <dl> <dt>BootEventCollectorWMI.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>BEvtCol.exe</dt> </dl>               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Control**](control.md)
</dt> </dl>

 

