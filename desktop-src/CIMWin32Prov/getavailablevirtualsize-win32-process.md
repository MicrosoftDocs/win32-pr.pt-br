---
description: Recupera o tamanho atual, em bytes, do espaço de endereço virtual livre disponível para o processo.
ms.assetid: 13b3b347-5db1-484f-bd1d-3a604eb6bc5b
ms.tgt_platform: multiple
title: Método GetAvailableVirtualSize da classe Win32_Process dados
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.GetAvailableVirtualSize
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7cdea363ce835297469242a4166d5e1e9eeea0845f27d0c780eef88f775bf751
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118675988"
---
# <a name="getavailablevirtualsize-method-of-the-win32_process-class"></a>Método GetAvailableVirtualSize da classe Process Win32 \_

Recupera o tamanho atual, em bytes, do espaço de endereço virtual livre disponível para o processo.

## <a name="syntax"></a>Sintaxe


```mof
uint32 GetAvailableVirtualSize(
  [out] uint64 AvailableVirtualSize
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*AvailableVirtualSize* \[ out\]
</dt> <dd>

O *parâmetro AvailableVirtualSize* retorna o espaço de endereço virtual gratuito disponível para esse processo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna zero (0) para indicar êxito. Qualquer outro número indica um erro. Para obter códigos de erro adicionais, [**consulte Constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para valores **gerais de HRESULT,** consulte [Códigos de erro do sistema.](/windows/desktop/Debug/system-error-codes)

<dl> <dt>

**Conclusão bem-sucedida**
</dt> <dd>

0

A operação foi concluída com sucesso.

</dd> <dt>

**Acesso negado**
</dt> <dd>

2

O usuário não tem acesso às informações solicitadas

</dd> <dt>

**Privilégio insuficiente**
</dt> <dd>

3

O usuário não tem privilégios suficientes.

</dd> <dt>

**Falha desconhecida**
</dt> <dd>

8

Falha desconhecida.

</dd> <dt>

**demarcador não localizado**
</dt> <dd>

9

O caminho especificado não existe.

</dd> <dt>

**Parâmetro inválido**
</dt> <dd>

21

O parâmetro especificado é inválido.

</dd> <dt>

**Outras**
</dt> <dd>

22 4294967295

Para valores diferentes daqueles listados, consulte a [documentação códigos de erro do](/windows/desktop/Debug/system-error-codes) sistema.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1<br/>                                                                  |
| Servidor mínimo com suporte<br/> | Windows Server 2012 R2<br/>                                                       |
| Namespace<br/>                | RAIZ \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Processo \_ win32**](win32-process.md)
</dt> </dl>

 

