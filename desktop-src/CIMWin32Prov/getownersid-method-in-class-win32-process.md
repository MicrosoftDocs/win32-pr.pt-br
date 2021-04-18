---
description: O getownerid&\# 8194; O método de classe WMI recupera o SID (identificador de segurança) para o proprietário desse processo.
ms.assetid: f856b06c-8080-4145-a775-51361f741873
ms.tgt_platform: multiple
title: Método getownerid da classe Win32_Process
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.GetOwnerSid
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c3ed34d132d363c0ce9f83511459ec40f340a06c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105755197"
---
# <a name="getownersid-method-of-the-win32_process-class"></a>Método getownerid da classe de \_ processo do Win32

O método de classe **Getownerid** [WMI](/windows/desktop/WmiSdk/retrieving-a-class) recupera o Sid (identificador de segurança) para o proprietário desse processo.

Este tópico usa a sintaxe formato MOF (MOF). Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxe


```mof
uint32 GetOwnerSid(
  [out] string Sid
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Sid* \[ do fora\]
</dt> <dd>

Retorna o descritor do identificador de segurança para este processo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna zero (0) para indicar êxito. Qualquer outro número indica um erro. Para obter códigos de erro adicionais, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Conclusão bem-sucedida** (0)
</dt> <dt>

**Acesso negado** (2)
</dt> <dt>

**Privilégio insuficiente** (3)
</dt> <dt>

**Falha desconhecida** (8)
</dt> <dt>

**Caminho não encontrado** (9)
</dt> <dt>

**Parâmetro inválido** (21)
</dt> <dt>

**Outro** (22 4294967295)
</dt> </dl>

## <a name="examples"></a>Exemplos

O exemplo de código do PowerShell [localizar os usuários conectados em um sistema remoto/s versão 2](https://Gallery.TechNet.Microsoft.Com/Find-the-logged-on-users-1161bd92) consulta computadores remotos para ver quem está conectado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Raiz \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**\_Processo Win32**](win32-process.md)
</dt> </dl>

 

