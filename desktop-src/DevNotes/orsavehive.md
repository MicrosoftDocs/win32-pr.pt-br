---
description: Grava o hive do registro offline especificado em um arquivo.
ms.assetid: 26f2eed9-e6e0-4dc0-8b91-212cde072744
title: Função ORSaveHive (Offreg.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORSaveHive
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 0b4dde44b6cc6d2c5cfd80f4041cd6370f680eb6ca867e9e8f2bbce5f0702e27
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119758506"
---
# <a name="orsavehive-function"></a>Função ORSaveHive

Grava o hive do registro offline especificado em um arquivo.

## <a name="syntax"></a>Sintaxe


```C++
DWORD ORSaveHive(
  _In_ ORHKEY Handle,
  _In_ PCWSTR lpHivePath,
  _In_ DWORD  dwOsMajorVersion,
  _In_ DWORD  dwOsMinorVersion
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Manipular* \[ Em\]
</dt> <dd>

Um handle para o hive do registro offline a ser salvo.

</dd> <dt>

*lpHivePath* \[ Em\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres Unicode que especifica o nome do arquivo hive do Registro. Esse não pode ser o nome de um arquivo existente.

</dd> <dt>

*dwOsMajorVersion* \[ Em\]
</dt> <dd>

O número de versão principal do sistema operacional. Esse membro pode ser um dos valores a seguir.



| Valor                                                                        | Significado                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>5</dt> </dl> | Se *dwOsMinorVersion* for 1, o sistema operacional será Windows XP.<br/> Se *dwOsMinorVersion* for 2, o sistema operacional será Windows Server 2003 R2, Windows Server 2003 ou Windows XP Professional x64 Edition.<br/> |
| <dl> <dt>6</dt> </dl> | Se *dwOsMinorVersion* for 0, o sistema operacional será Windows Server 2008 ou Windows Vista.<br/> Se *dwOsMinorVersion* for 1, o sistema operacional será Windows Server 2008 R2 ou Windows 7.<br/>                       |



 

</dd> <dt>

*dwOsMinorVersion* \[ Em\]
</dt> <dd>

O número de versão secundária do sistema operacional. Esse membro pode ser um dos valores a seguir.



| Valor                                                                        | Significado                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Se *dwOsMajorVersion* for 6, o sistema operacional será Windows Server 2008 ou Windows Vista.<br/>                                                                                                                                          |
| <dl> <dt>1</dt> </dl> | Se *dwOsMajorVersion* for 5, o sistema operacional será Windows XP.<br/> Se *dwOsMajorVersion* for 6, o sistema operacional será Windows Server 2008 R2 ou Windows 7.<br/>                                                                |
| <dl> <dt>2</dt> </dl> | Se *dwOsMajorVersion* for 5, o sistema operacional será Windows Server 2003 R2, Windows Server 2003 ou Windows XP Professional x64 Edition. <br/> Se *dwOsMajorVersion* for 6, o *parâmetro dwOsMinorVersion* deverá ser 0 ou 1. <br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será ERROR \_ SUCCESS.

Se a função falhar, o valor de retorno será um código de erro não zero definido em Winerror.h. Você pode usar a [função FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) com o sinalizador FORMAT MESSAGE FROM SYSTEM para obter \_ uma \_ \_ descrição genérica do erro. Os códigos de erro possíveis incluem o seguinte:

-   Se o chamador não tiver os direitos de acesso necessários para gravar o arquivo, a função retornará ERROR \_ ACCESS \_ DENIED.
-   Se o arquivo especificado já existir, a função retornará ERROR \_ ALREADY \_ EXISTS.

## <a name="remarks"></a>Comentários

A **função ORSaveHive** deve ser usada para salvar as alterações feitas em um hive de registro offline. As alterações não são preservadas até **que ORSaveHive** seja chamado para salvar o hive em um arquivo.

Os *parâmetros dwOsMajorVersion* e *dwOsMinorVersion* juntos especificam o formato de destino do arquivo hive do Registro. A tabela a seguir resume os números de versão mais recentes do sistema operacional.



| Sistema operacional                    | Número de versão |
|-------------------------------------|----------------|
| Windows Server 2008 R2              | 6.1            |
| Windows 7                           | 6.1            |
| Windows Server 2008                 | 6,0            |
| Windows Vista                       | 6,0            |
| Windows Server 2003 R2              | 5.2            |
| Windows Server 2003                 | 5.2            |
| Windows XP Professional x64 Edition | 5.2            |
| Windows XP                          | 5.1            |



 

Use a [função GetVersionEx](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa) para recuperar informações sobre o sistema operacional atual.

A **função ORSaveHive** bloqueia o hive do Registro enquanto ele está escrevendo o hive no arquivo e, em seguida, fecha o arquivo e libera o bloqueio. O hive do Registro permanece na memória até que seja fechado chamando a [**função ORCloseHive.**](orclosehive.md) É possível fazer outras alterações no hive do Registro enquanto ele está aberto; no entanto, para preservar essas alterações, o hive deve ser salvo em um novo arquivo, porque a **função ORSaveHive** não substituirá um arquivo existente.

A **função ORSaveHive** pode ser usada para salvar parte do hive do registro offline. A chave especificada no parâmetro *Handle* torna-se a chave raiz de um hive que consiste na chave especificada e em todas as suas sub-chaves.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|---------------------------------------------------------------------------------------|
| Redistribuível<br/> | Windows Biblioteca de Registro offline versão 1.0 ou posterior<br/>                      |
| Cabeçalho<br/>          | <dl> <dt>Offreg.h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Getversionex](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa)
</dt> <dt>

[**ORCloseHive**](orclosehive.md)
</dt> <dt>

[**OROpenHive**](oropenhive.md)
</dt> </dl>

 

 
