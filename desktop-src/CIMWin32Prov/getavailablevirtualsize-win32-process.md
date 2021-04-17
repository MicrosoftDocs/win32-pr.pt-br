---
description: Recupera o tamanho atual, em bytes, do espaço de endereço virtual livre disponível para o processo.
ms.assetid: 13b3b347-5db1-484f-bd1d-3a604eb6bc5b
ms.tgt_platform: multiple
title: Método GetAvailableVirtualSize da classe Win32_Process
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
ms.openlocfilehash: ee6e798b8df32822de481f3af1dc6b21a81d1024
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756254"
---
# <a name="getavailablevirtualsize-method-of-the-win32_process-class"></a>Método GetAvailableVirtualSize da \_ classe Process do Win32

Recupera o tamanho atual, em bytes, do espaço de endereço virtual livre disponível para o processo.

## <a name="syntax"></a>Sintaxe


```mof
uint32 GetAvailableVirtualSize(
  [out] uint64 AvailableVirtualSize
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*AvailableVirtualSize* \[ fora\]
</dt> <dd>

O parâmetro *AvailableVirtualSize* retorna o espaço de endereço virtual livre disponível para esse processo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna zero (0) para indicar êxito. Qualquer outro número indica um erro. Para obter códigos de erro adicionais, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).

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

Para valores diferentes daqueles listados, consulte a documentação de [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes) .

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1<br/>                                                                  |
| Servidor mínimo com suporte<br/> | Windows Server 2012 R2<br/>                                                       |
| Namespace<br/>                | Raiz \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_Processo Win32**](win32-process.md)
</dt> </dl>

 

