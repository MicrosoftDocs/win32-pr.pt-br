---
description: Este tópico descreve os limites de memória para versões Windows e Windows Server com suporte.
ms.assetid: de09c8af-0ed8-4fd4-b8e8-2c921aafe6f2
title: Limites de memória para as versões do Windows e do Windows Server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8d2b11b636fcbcd3338986aa4ce88388f3b722045eee895e4acb1b62d5920eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117992748"
---
# <a name="memory-limits-for-windows-and-windows-server-releases"></a>Limites de memória para as versões do Windows e do Windows Server

Este tópico descreve os limites de memória para versões Windows e Windows Server com suporte.

-   [Limites de espaço de memória e endereço](#memory-limits-for-windows-and-windows-server-releases)
-   [Limites de memória física: Windows 10](#physical-memory-limits-windows-10)
-   [Limites de memória física: Windows Server 2016](#physical-memory-limits-windows-server-2016)
-   [Limites de memória física: Windows 8](#physical-memory-limits-windows-8)
-   [Limites de memória física: Windows Server 2012](#physical-memory-limits-windows-server-2012)
-   [Limites de memória física: Windows 7](#physical-memory-limits-windows-7)
-   [Limites de memória física: Windows Server 2008 R2](#physical-memory-limits-windows-server-2008-r2)
-   [Limites de memória física: Windows Server 2008](#physical-memory-limits-windows-server-2008-r2)
-   [Limites de memória física: Windows Vista](#physical-memory-limits-windows-vista)
-   [Limites de memória física: Windows Home Server](#physical-memory-limits-windows-home-server)
-   [Limites de memória física: Windows Server 2003 R2](#physical-memory-limits-windows-server-2003-r2)
-   [Limites de memória física: Windows Server 2003 com Service Pack 2 (SP2)](#physical-memory-limits-windows-server-2003-with-service-pack-2-sp2)
-   [Limites de memória física: Windows Server 2003 com Service Pack 1 (SP1)](#physical-memory-limits-windows-server-2003-with-service-pack-1-sp1)
-   [Limites de memória física: Windows Server 2003](#physical-memory-limits-windows-server-2003-r2)
-   [Limites de memória física: Windows XP](#physical-memory-limits-windows-xp)
-   [Limites de memória física: Windows Inserido](#physical-memory-limits-windows-embedded)
-   [Como as placas gráficas e outros dispositivos afetam os limites de memória](#how-graphics-cards-and-other-devices-affect-memory-limits)
-   [Tópicos relacionados](#related-topics)

Os limites de memória e espaço de endereço variam de acordo com a plataforma, o sistema operacional e se o valor **IMAGE FILE LARGE ADDRESS \_ \_ \_ \_ AWARE** da estrutura [**DE \_ IMAGEM**](/windows/win32/api/dbghelp/ns-dbghelp-loaded_image) CARREGADA e o ajuste [de 4 GIGabyte](4-gigabyte-tuning.md) (4GT) estão em uso. **IMAGE \_ FILE \_ LARGE \_ ADDRESS \_ AWARE** é definido ou limpo usando a opção de linker [/LARGEADDRESSAWARE.](/cpp/build/reference/largeaddressaware-handle-large-addresses?view=vs-2019)

O ajuste de 4 gigabyte (4GT), também conhecido como ajuste de memória do aplicativo ou a opção /3 GB, é uma tecnologia (aplicável somente a sistemas de 32 bits) que altera a quantidade de espaço de endereço virtual disponível para aplicativos de modo de usuário. A habilitação dessa tecnologia reduz o tamanho geral do espaço de endereço virtual do sistema e, portanto, os máximos de recursos do sistema. Para obter mais informações, consulte [O que é 4GT.]( /previous-versions/windows/it-pro/windows-server-2003/cc786709(v=ws.10))

Os limites de memória física para plataformas de 32 bits também dependem da PAE [(Extensão](physical-address-extension.md) de Endereço Físico), que permite que sistemas de Windows de 32 bits usem mais de 4 GB de memória física.

## <a name="memory-and-address-space-limits"></a>Limites de espaço de memória e endereço

A tabela a seguir especifica os limites de memória e espaço de endereço para versões com suporte do Windows. A menos que seja o contrário, os limites nesta tabela se aplicam a todas as versões com suporte.



| Tipo de memória                                                                                   | Limite no X86                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | Limite em 64 bits Windows                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Espaço de endereço virtual no modo de usuário para cada processo de 32 bits<br/>                            | 2 GB<br/> Até 3 GB com ARQUIVO DE IMAGEM COM SUPORTE **\_ A \_ \_ \_ ENDEREÇOS GRANDES** e 4GT<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       | 2 GB com **ARQUIVO DE IMAGEM COM O NOME DE ENDEREÇO GRANDE \_ \_ \_ \_ limpo** (padrão)<br/> 4 GB com ARQUIVO **DE IMAGEM DEFINIDO COM CONHECIMENTO DE \_ \_ \_ \_ ENDEREÇO** GRANDE<br/>                                                                                                                                                                                                                                                                                                                                                                 |
| Espaço de endereço virtual no modo de usuário para cada processo de 64 bits<br/>                            | Não se aplica<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              | **Com IMAGE \_ CONJUNTO \_ FILE LARGE ADDRESS \_ \_ AWARE** (padrão):<br/> **x64: Windows 8.1 e Windows Server 2012 R2 ou posterior:** 128 TB<br/> **x64: Windows 8 e Windows Server 2012 ou 8** TB anteriores<br/> **Sistemas baseados em Intel Itanium:** 7 TB<br/> <br/> 2 GB com ARQUIVO **DE IMAGEM COM O NOME DE ENDEREÇO GRANDE \_ \_ \_ \_ LIMPO**<br/>                                                                                                                                                                                              |
| Espaço de endereço virtual no modo kernel<br/>                                                  | 2 GB<br/> De 1 GB a um máximo de 2 GB com 4GT<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              | **Windows 8.1 e Windows Server 2012 R2 ou posterior:** 128 TB<br/> **Windows 8 e Windows Server 2012 ou 8** TB anteriores <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Pool de páginas<br/>                                                                         | 384 GB ou limite de commit do sistema, o que for menor. **Windows 8.1 e Windows Server 2012 R2:** 15,5 TB ou limite de commit do sistema, o que for menor. <br/> **Windows Server 2008 R2, Windows 7, Windows Server 2008 e Windows Vista:** Limitado pelo espaço de endereço virtual no modo kernel disponível. Começando com Windows Vista com Service Pack 1 (SP1), o pool de páginas também pode ser limitado pelo valor da chave do Registro [PagedPoolLimit.](memory-management-registry-keys.md)<br/> **Windows Home Server e Windows Server 2003:** 530 MB<br/> **Windows XP:** 490 MB<br/> <br/>                                                                                                 | 384 GB ou limite de commit do sistema, o que for menor Windows 8.1 e **Windows Server 2012 R2:** 15,5 TB ou limite de commit do sistema, o que for menor. <br/> **Windows Server 2008 R2, Windows 7, Windows Server 2008** e Windows Vista: 128 GB ou limite de commit do sistema, o que for menor<br/> **Windows Server 2003 e Windows XP:** Até 128 GB, dependendo da configuração e da RAM.<br/> <br/>                                                                                |
| Pool não pa pa pagado<br/>                                                                      | 75% de RAM ou 2 GB, o que for menor. **Windows 8.1 e Windows Server 2012 R2:** RAM ou 16 TB, o que for menor (o espaço de endereço é limitado a 2 x RAM).<br/> **Windows Vista:** Limitado apenas pelo espaço de endereço virtual do modo kernel e pela memória física. A partir do Windows Vista com SP1, o pool não papagado também pode ser limitado pelo valor da chave do Registro [NonPagedPoolLimit.](memory-management-registry-keys.md)<br/> **Windows Home Server, Windows Server 2003 e Windows XP:** 256 MB ou 128 MB com 4GT.<br/> <br/>                                                                                                                                                 | RAM ou 128 GB, o que for menor (o espaço de endereço é limitado a 2 x RAM) Windows 8.1 e **Windows Server 2012 R2:** RAM ou 16 TB, o que for menor (o espaço de endereço é limitado a 2 x RAM).<br/> **Windows Server 2008 R2, Windows 7 e Windows Server 2008:** 75% de RAM até um máximo de 128 GB<br/> **Windows Vista:** 40% da RAM até um máximo de 128 GB.<br/> **Windows Server 2003 e Windows XP:** Até 128 GB, dependendo da configuração e da RAM.<br/> <br/> |
| Espaço de endereço virtual do cache do sistema (tamanho físico limitado apenas pela memória física)<br/> | Limitado pelo espaço de endereço virtual no modo kernel disponível ou pelo valor da chave do Registro [SystemCacheLimit.](memory-management-registry-keys.md)<br/> **Windows 8.1 e Windows Server 2012 R2:** 16 TB.<br/> **Windows Vista:** Limitado apenas pelo espaço de endereço virtual do modo kernel. A partir do Windows Vista com SP1, o espaço de endereço virtual do cache do sistema também pode ser limitado pelo valor da chave do Registro [SystemCacheLimit.](memory-management-registry-keys.md)<br/> **Windows Home Server, Windows Server 2003** e Windows XP: 860 MB com a chave do Registro [LargeSystemCache](/previous-versions/windows/it-pro/windows-server-2003/cc784562(v=ws.10)) definida e sem 4GT; até 448 MB com 4GT.<br/> <br/> | Sempre 1 TB, independentemente da ram **física Windows 8.1 e Windows Server 2012 R2:** 16 TB.<br/> **Windows Server 2003 e Windows XP:** Até 1 TB, dependendo da configuração e da RAM.<br/> <br/>                                                                                                                                                                                                                                                                                            |



 

## <a name="physical-memory-limits-windows-10"></a>Limites de memória física: Windows 10

A tabela a seguir especifica os limites de memória física para Windows 10.



| Versão               | Limite no X86    | Limite em X64     |
|-----------------------|-----------------|------------------|
| Windows 10 Enterprise | 4 GB<br/> | 6 TB<br/>   |
| Windows 10 Education  | 4 GB<br/> | 2 TB<br/>   |
| Windows 10 Pro for Workstations  | 4 GB<br/> | 6 TB<br/>   |
| Windows 10 Pro        | 4 GB<br/> | 2 TB<br/>   |
| Windows 10 Home       | 4 GB<br/> | 128 GB<br/> |



 

## <a name="physical-memory-limits-windows-server-2016"></a>Limites de memória física: Windows Server 2016

A tabela a seguir especifica os limites de memória física para Windows Server 2016.



| Versão                        | Limite em X64     |
|--------------------------------|------------------|
| Windows Server 2016 Datacenter | 24 TB<br/> |
| Windows Server 2016 Standard   | 24 TB<br/> |



 

## <a name="physical-memory-limits-windows-8"></a>Limites de memória física: Windows 8

A tabela a seguir especifica os limites de memória física para Windows 8.



| Versão                | Limite no X86    | Limite em X64      |
|------------------------|-----------------|-------------------|
| O Windows 8 Enterprise   | 4 GB<br/> | 512 GB<br/> |
| Windows 8 Professional | 4 GB<br/> | 512 GB<br/> |
| Windows 8              | 4 GB<br/> | 128 GB<br/> |



 

## <a name="physical-memory-limits-windows-server-2012"></a>Limites de memória física: Windows Server 2012

A tabela a seguir especifica os limites de memória física para Windows Server 2012. Windows Server 2012 está disponível apenas em edições X64.



| Versão                               | Limite em X64     |
|---------------------------------------|------------------|
| Windows Server 2012 Datacenter        | 4 TB<br/>  |
| Windows Server 2012 Standard          | 4 TB<br/>  |
| Windows Server 2012 Essentials        | 64 GB<br/> |
| Windows Server 2012 Foundation        | 32 GB<br/> |
| Grupo de trabalho do Windows Storage Server 2012 | 32 GB<br/> |
| Windows Storage Server 2012 Standard  | 4 TB<br/>  |
| Hyper-V Server 2012                   | 4 TB<br/>  |



 

## <a name="physical-memory-limits-windows-7"></a>Limites de memória física: Windows 7

A tabela a seguir especifica os limites de memória física para Windows 7.



| Versão                | Limite no X86    | Limite em X64      |
|------------------------|-----------------|-------------------|
| Windows 7 Ultimate     | 4 GB<br/> | 192 GB<br/> |
| Windows 7 Enterprise   | 4 GB<br/> | 192 GB<br/> |
| Windows 7 Professional | 4 GB<br/> | 192 GB<br/> |
| Windows 7 Home Premium | 4 GB<br/> | 16 GB<br/>  |
| Windows 7 Home Basic   | 4 GB<br/> | 8 GB<br/>   |
| Windows 7 Starter      | 2 GB<br/> | N/D<br/>    |



 

## <a name="physical-memory-limits-windows-server-2008-r2"></a>Limites de memória física: Windows Server 2008 R2

A tabela a seguir especifica os limites de memória física para Windows Server 2008 R2. Windows O Servidor 2008 R2 está disponível somente em edições de 64 bits.



| Versão                                          | Limite em X64      | Limite em IA64   |
|--------------------------------------------------|-------------------|-----------------|
| Windows Server 2008 R2 Datacenter                | 2 TB<br/>   |                 |
| Windows Server 2008 R2 Enterprise                | 2 TB<br/>   |                 |
| Windows Server 2008 R2 for Itanium-Based Systems |                   | 2 TB<br/> |
| Windows Server 2008 R2 Foundation                | 8 GB<br/>   |                 |
| Windows Server 2008 R2 Standard                  | 32 GB<br/>  |                 |
| Windows HPC Server 2008 R2                       | 128 GB<br/> |                 |
| Windows Web Server 2008 R2                       | 32 GB<br/>  |                 |



 

## <a name="physical-memory-limits-windows-server-2008"></a>Limites de memória física: Windows Server 2008

A tabela a seguir especifica os limites de memória física para Windows Server 2008. Limites maiores que 4 GB para 32 bits Windows suponha que [a PAE](physical-address-extension.md) está habilitada.



| Versão                                       | Limite no X86     | Limite em X64      | Limite em IA64   |
|-----------------------------------------------|------------------|-------------------|-----------------|
| Windows Server 2008 Datacenter                | 64 GB<br/> | 1 TB<br/>   |                 |
| Windows Server 2008 Enterprise                | 64 GB<br/> | 1 TB<br/>   |                 |
| Windows Server 2008 HPC Edition               |                  | 128 GB<br/> |                 |
| Windows Server 2008 Standard                  | 4 GB<br/>  | 32 GB<br/>  |                 |
| Windows Server 2008 for Itanium-Based Systems |                  |                   | 2 TB<br/> |
| Windows Small Business Server 2008            | 4 GB<br/>  | 32 GB<br/>  |                 |
| Windows Web Server 2008                       | 4 GB<br/>  | 32 GB<br/>  |                 |



 

## <a name="physical-memory-limits-windows-vista"></a>Limites de memória física: Windows Vista

A tabela a seguir especifica os limites de memória física para Windows Vista.



| Versão                    | Limite no X86    | Limite em X64      |
|----------------------------|-----------------|-------------------|
| Windows Vista Ultimate     | 4 GB<br/> | 128 GB<br/> |
| Windows Vista Enterprise   | 4 GB<br/> | 128 GB<br/> |
| Windows Vista Business     | 4 GB<br/> | 128 GB<br/> |
| Windows Vista Home Premium | 4 GB<br/> | 16 GB<br/>  |
| Windows Vista Home Basic   | 4 GB<br/> | 8 GB<br/>   |
| Windows Vista Starter      | 1 GB<br/> |                   |



 

## <a name="physical-memory-limits-windows-home-server"></a>Limites de memória física: Windows Home Server

Windows O Home Server está disponível apenas em uma edição de 32 bits. O limite de memória física é de 4 GB.

## <a name="physical-memory-limits-windows-server-2003-r2"></a>Limites de memória física: Windows Server 2003 R2

A tabela a seguir especifica os limites de memória física para Windows Server 2003 R2. Limites acima de 4 GB para 32 bits Windows suponha que [a PAE](physical-address-extension.md) está habilitada.



| Versão                                              | Limite no X86                                 | Limite em X64     |
|------------------------------------------------------|----------------------------------------------|------------------|
| Windows Server 2003 R2 Datacenter Edition<br/> | 64 GB<br/> (16 GB com 4GT)<br/> | 1 TB<br/>  |
| Windows Servidor 2003 R2 Edição Enterprise<br/> | 64 GB<br/> (16 GB com 4GT)<br/> | 1 TB<br/>  |
| Windows Server 2003 R2 Standard Edition<br/>   | 4 GB<br/>                              | 32 GB<br/> |



 

## <a name="physical-memory-limits-windows-server-2003-with-service-pack-2-sp2"></a>Limites de memória física: Windows Server 2003 com Service Pack 2 (SP2)

A tabela a seguir especifica os limites de memória física para o Windows Server 2003 com o Service Pack 2 (SP2). Limites acima de 4 GB para 32 bits Windows suponha que [a PAE](physical-address-extension.md) está habilitada.



| Versão                                                                      | Limite no X86                                 | Limite em X64     | Limite em IA64   |
|------------------------------------------------------------------------------|----------------------------------------------|------------------|-----------------|
| Windows Server 2003 com Service Pack 2 (SP2), Datacenter Edition<br/> | 64 GB<br/> (16 GB com 4GT)<br/> | 1 TB<br/>  | 2 TB<br/> |
| Windows Server 2003 com Service Pack 2 (SP2), Edição Enterprise<br/> | 64 GB<br/> (16 GB com 4GT)<br/> | 1 TB<br/>  | 2 TB<br/> |
| Windows Server 2003 com Service Pack 2 (SP2), Edição Standard<br/>   | 4 GB<br/>                              | 32 GB<br/> |                 |



 

## <a name="physical-memory-limits-windows-server-2003-with-service-pack-1-sp1"></a>Limites de memória física: Windows Server 2003 com Service Pack 1 (SP1)

A tabela a seguir especifica os limites de memória física para Windows Server 2003 com Service Pack 1 (SP1). Limites acima de 4 GB para 32 bits Windows suponha que [a PAE](physical-address-extension.md) está habilitada.



| Versão                                                                      | Limite no X86                                 | Limite em X64        | Limite em IA64   |
|------------------------------------------------------------------------------|----------------------------------------------|---------------------|-----------------|
| Windows Server 2003 com Service Pack 1 (SP1), Datacenter Edition<br/> | 64 GB<br/> (16 GB com 4GT)<br/> | X64 1 TB<br/> | 1 TB<br/> |
| Windows Server 2003 com Service Pack 1 (SP1), Edição Enterprise<br/> | 64 GB<br/> (16 GB com 4GT)<br/> | X64 1 TB<br/> | 1 TB<br/> |
| Windows Server 2003 com Service Pack 1 (SP1), Edição Standard<br/>   | 4 GB<br/>                              | 32 GB<br/>    |                 |



 

## <a name="physical-memory-limits-windows-server-2003"></a>Limites de memória física: Windows Server 2003

A tabela a seguir especifica os limites de memória física para Windows Server 2003. Limites acima de 4 GB para 32 bits Windows suponha que [a PAE](physical-address-extension.md) está habilitada.



| Versão                                                    | Limite no X86                                 | Limite em IA64     |
|------------------------------------------------------------|----------------------------------------------|-------------------|
| Windows Server 2003, Datacenter Edition<br/>         | 64 GB<br/> (16 GB com 4GT)<br/> | 512 GB<br/> |
| Windows Server 2003, Enterprise Edition<br/>         | 64 GB<br/> (16 GB com 4GT)<br/> | 512 GB<br/> |
| Windows Server 2003, Standard Edition<br/>           | 4 GB<br/>                              |                   |
| Windows Server 2003, Web Edition<br/>                | 2 GB<br/>                              |                   |
| Windows Small Business Server 2003<br/>              | 4 GB<br/>                              |                   |
| Windows Compute Cluster Server 2003<br/>             |                                              | 32 GB<br/>  |
| Windows Armazenamento Server 2003, Edição Enterprise<br/> | 8 GB<br/>                              |                   |
| Windows Storage Server 2003<br/>                     | 4 GB<br/>                              |                   |



 

## <a name="physical-memory-limits-windows-xp"></a>Limites de memória física: Windows XP

A tabela a seguir especifica os limites de memória física para Windows XP.



| Versão                    | Limite no X86      | Limite em X64      | Limite em IA64                     |
|----------------------------|-------------------|-------------------|-----------------------------------|
| Windows XP                 | 4 GB<br/>   | 128 GB<br/> | 128 GB (sem suporte)<br/> |
| Windows XP Starter Edition | 512 MB<br/> | N/D<br/>    | N/D<br/>                    |



 

## <a name="physical-memory-limits-windows-embedded"></a>Limites de memória física: Windows inserido

A tabela a seguir especifica os limites de memória física para Windows Embedded.



| Versão                                   | Limite no X86    | Limite em X64      |
|-------------------------------------------|-----------------|-------------------|
| Windows XP Embedded<br/>            | 4 GB<br/> |                   |
| Windows Embedded Standard 2009<br/> | 4 GB<br/> |                   |
| Windows Embedded Standard 7<br/>    | 4 GB<br/> | 192 GB<br/> |



 

## <a name="how-graphics-cards-and-other-devices-affect-memory-limits"></a>Como as placas gráficas e outros dispositivos afetam os limites de memória

Os dispositivos têm que mapear sua memória abaixo de 4 GB para compatibilidade com versões que não têm suporte para PAE Windows versões. Portanto, se o sistema tiver 4 GB de RAM, alguns deles são desabilitados ou remapped acima de 4 GB pelo BIOS. Se a memória for remapped, o Windows X64 poderá usar essa memória. As versões de cliente X86 do Windows não são suportadas com memória física acima da marca de 4 GB, portanto, elas não podem acessar essas regiões remapeadas. Qualquer versão X64 Windows ou X86 Server pode.

As versões do cliente X86 com PAE habilitada têm um espaço de endereço físico de 128 GB (37 bits) acessível. O limite que essas versões impõem é o endereço ram físico mais alto permitido, não o tamanho do espaço de E/S. Isso significa que os drivers com suporte a PAE podem realmente usar espaço físico acima de 4 GB se quiserem. Por exemplo, os drivers podem mapear as regiões de memória "perdidas" localizadas acima de 4 GB e expor essa memória como um disco ram.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Ajuste de 4 gigabyte](4-gigabyte-tuning.md)
</dt> <dt>

[**ARQUIVO DE \_ IMAGEM COM GRANDE CONHECIMENTO DE \_ \_ \_ ENDEREÇO**](/windows/win32/api/dbghelp/ns-dbghelp-loaded_image)
</dt> <dt>

[Extensão de endereço físico](physical-address-extension.md)
</dt> </dl>

 

 
