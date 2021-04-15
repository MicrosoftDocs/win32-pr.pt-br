---
title: Chave de ProgID independente de versão
description: Associa um ProgID a um CLSID. Essa chave é usada para determinar a versão mais recente de um aplicativo de objeto.
ms.assetid: fb43c8d0-d923-487f-afdf-14fc29a71e0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0a0bf379a06a6a05bb69a232ef91bb9fe81dc2f
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104454544"
---
# <a name="version-independent-progid-key"></a>Chave de ProgID independente de versão

Associa um ProgID a um CLSID. Essa chave é usada para determinar a versão mais recente de um aplicativo de objeto.

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes
   <version-independent ProgID>
      CurVer = ProgID
```

## <a name="remarks"></a>Comentários

A chave **HKEY \_ local \_ Machine \\ software \\ classes** corresponde à chave de **\_ \_ raiz de classes hKey** , que foi retida para compatibilidade com versões anteriores do com.

O formato para <*ProgID> de versão* é <*programa*>. <*componente*>, separado por pontos, sem espaços e nenhum número de versão. O ProgID independente de versão, como o ProgID, pode ser registrado com um nome legível.

*ProgID* é o ProgID da versão mais recente instalada da classe.

Os aplicativos devem registrar um identificador programático independente de versão sob a chave *ProgID independente de versão* . O ProgID independente de versão refere-se à classe do aplicativo e não muda de versão para versão, em vez disso, constante restante em todos os versionsâ € "por exemplo, documento do Microsoft Word. Ele é usado com linguagens de macro e refere-se à versão atualmente instalada da classe do aplicativo. O ProgID independente de versão deve corresponder ao nome da versão mais recente do aplicativo de objeto.

Por exemplo, o ProgID independente de versão é usado quando um aplicativo de contêiner cria um gráfico ou uma tabela com um botão de barra de ferramentas. Nessa situação, o aplicativo pode usar o ProgID independente de versão para determinar a versão mais recente do aplicativo de objeto necessário.

O ProgID independente de versão é armazenado e mantido exclusivamente pelo código do aplicativo. Ao receber o ProgID independente de versão, a função [**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) retorna o CLSID da versão atual.

Você pode usar [**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) e [**ProgIDFromCLSID**](/windows/desktop/api/combaseapi/nf-combaseapi-progidfromclsid) para converter entre essas duas representações.

Você pode usar [**IOleObject:: GetUserType**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype) ou [**OleRegGetUserType**](/windows/desktop/api/Ole2/nf-ole2-olereggetusertype) para alterar o identificador para uma cadeia de caracteres que pode ser reproduzida.

Se um manipulador personalizado não for usado, a entrada deverá ser definida como OLE32.DLL, conforme mostrado no exemplo a seguir:

```
HKEY_CLASSES_ROOT\CLSID\{00000402-0000-0000-C000-000000000046}
   InprocHandler = ole32.dll
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid)
</dt> <dt>

[**ProgIDFromCLSID**](/windows/desktop/api/combaseapi/nf-combaseapi-progidfromclsid)
</dt> <dt>

[<ProgID> Chaves](-progid--key.md)
</dt> </dl>

 

 




