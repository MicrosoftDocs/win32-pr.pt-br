---
description: Obtém os direitos de acesso remoto para uma lista de usuários individuais em computadores que executam versões obsoletas do Windows, em que o controle de acesso por meio de descritores de segurança do Windows não está disponível.
ms.assetid: 79a596db-5f85-4664-8989-f309286eca0d
ms.tgt_platform: multiple
title: 'Método __SystemSecurity:: Get9XUserList'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.Get9XUserList
api_type:
- COM
api_location:
- all
ms.openlocfilehash: 521f2fe489089d486480c138293ebea39ca6f105
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105749396"
---
# <a name="__systemsecurityget9xuserlist-method"></a>\_\_Método SystemSecurity:: Get9XUserList

O método [**\_ \_ SystemSecurity:: Set9XUserList**](--systemsecurity-set9xuserlist.md) Obtém os direitos de acesso remoto para uma lista de usuários individuais em computadores que executam versões obsoletas do Windows, em que o controle de acesso por meio de descritores de segurança do Windows não está disponível.

Isso funciona de forma semelhante ao descritor de segurança, mas é mais limitado. Não há suporte para grupos e não há nenhum controle sobre o acesso local, pois o usuário local sempre tem acesso completo. Tanto a negação quanto as entradas de controle de acesso (ACE) são permitidas e, por isso, a ordem de ACE é importante na DACL (lista de controle de acesso discricionário). Para obter mais informações, consulte [ordem das ACEs em uma DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Get9XUserList(
  [out] __NTLMUser9X ul[]
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*UL* \[ fora\]
</dt> <dd>

Matriz de usuários.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retorna um **HRESULT** que indica o status da chamada do método. A lista a seguir lista os valores de retorno que são de significância a **Get9XUserList**. Para aplicativos de script e Visual Basic, o resultado pode ser [Parameters. ReturnValue](parsing-outparameters-objects.md). Para obter mais informações, consulte [construindo objetos de inparâmetros e analisando objetos de Parameters](constructing-inparameters-objects-and-parsing-outparameters-objects.md).

<dl> <dt>

**\_método WBEM \_ E \_ desabilitado**
</dt> <dd>

Não há suporte para esse método em versões do Windows com suporte.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>       |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | todos os namespaces do WMI<br/>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Classes do sistema WMI](wmi-system-classes.md)
</dt> <dt>

[**\_\_SystemSecurity**](--systemsecurity.md)
</dt> <dt>

[**\_\_SystemSecurity:: Obtém-se**](--systemsecurity-getsd.md)
</dt> <dt>

[**\_\_SystemSecurity:: definido**](--systemsecurity-setsd.md)
</dt> <dt>

[**Ace do Win32 \_**](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
</dt> <dt>

[**\_SecurityDescriptor Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[Protegendo namespaces WMI](securing-wmi-namespaces.md)
</dt> <dt>

[Constantes de segurança do WMI](wmi-security-constants.md)
</dt> </dl>

 

